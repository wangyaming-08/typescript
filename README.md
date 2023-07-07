
`vue如何获取组件的类型`
```
import { ElForm } from 'element-plus'

const formRef = useCompRef(ElForm)
formRef.value?.validate()

import { ref } from 'vue'

export default function useCompRef<T extends abstract new () => any>(_comp: T) {
  return ref<InstanceType<T>>()
}
```