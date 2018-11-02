---
UID: NF:objidl.IAgileReference.Resolve(Q,)
title: IAgileReference::Resolve(Q,)
author: windows-sdk-content
description: Gets the interface ID of an agile reference to an object.
old-location: winrt\iagilereference_resolve.htm
tech.root: WinRT
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAgileReference interface [Windows Runtime],Resolve method, IAgileReference.Resolve, IAgileReference.Resolve(Q,), IAgileReference::Resolve, IAgileReference::Resolve(Q,), Resolve, Resolve method [Windows Runtime], Resolve method [Windows Runtime],IAgileReference interface, objidl/IAgileReference::Resolve, winrt.iagilereference_resolve
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IAgileReference.Resolve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAgileReference::Resolve(Q,)


## -description


Gets the interface ID of an agile reference to an object.


## -parameters




### -param pp

TBD


### -param arg1 [out, retval]

On successful completion, *<i>ppvObjectReference</i> is a pointer to the interface specified by <i>riid</i>.


#### - riid [in]

The interface ID of the interface to be retrieved from the agile reference. It is not required to be the same as the registered interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_NOINTERFACE</dt>
</dl>
</td>
<td width="60%">
The requested interface isn't implemented on the registered object.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a> function to create an agile reference to an object. Call the <b>Resolve</b> method to localize the object into the apartment in which <b>Resolve</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/51787A45-BCDE-4028-A338-1C16F2DE79AD">IAgileReference</a>



<a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a>
 

 

