---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPart::UnregisterControlChangeCallback


## -description



The <b>UnregisterControlChangeCallback</b> method removes the registration of an <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interface that the client previously registered by a call to the <a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">IPart::RegisterControlChangeCallback</a> method.




## -parameters




### -param pNotify [in]

Pointer to the <b>IControlChangeNotify</b> interface whose registration is to be deleted. The client passed this same interface pointer to the part object in a previous call to the <b>IPart::RegisterControlChangeCallback</b> method. If the <b>UnregisterControlChangeCallback</b> method succeeds, it calls the <b>Release</b> method on the client's <b>IControlChangeNotify</b> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Interface instance  <i>*pNotify</i> is not currently registered.

</td>
</tr>
</table>
 




## -remarks



Before the client releases its final reference to the <b>IControlChangeNotify</b> interface, it should call <b>UnregisterControlChangeCallback</b> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IControlChangeNotify</b> and <b>IPart</b> objects. Note that the <b>IPart::RegisterControlChangeCallback</b> method calls the client's <b>IControlChangeNotify::AddRef</b> method, and <b>UnregisterControlChangeCallback</b> calls the <b>IControlChangeNotify::Release</b> method. If the client errs by releasing its reference to the <b>IControlChangeNotify</b> interface before calling <b>UnregisterControlChangeCallback</b>, the <b>IPart</b> object never releases its reference to the <b>IControlChangeNotify</b> interface. For example, a poorly designed <b>IControlChangeNotify</b> implementation might call <b>UnregisterControlChangeCallback</b> from the destructor for the <b>IControlChangeNotify</b> object. In this case, the client will not call <b>UnregisterControlChangeCallback</b> until the <b>IPart</b> object releases its reference to the <b>IControlChangeNotify</b> interface, and the <b>IPart</b> object will not release its reference to the <b>IControlChangeNotify</b> interface until the client calls <b>UnregisterControlChangeCallback</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify Interface</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>



<a href="https://msdn.microsoft.com/58cf52c9-20ee-46c4-926e-c374a4f42240">IPart::RegisterControlChangeCallback</a>
 

 

