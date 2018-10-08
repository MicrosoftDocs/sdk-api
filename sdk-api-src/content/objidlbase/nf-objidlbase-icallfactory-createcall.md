---
UID: NF:objidlbase.ICallFactory.CreateCall
title: ICallFactory::CreateCall
author: windows-sdk-content
description: Creates an instance of the call object that corresponds to a specified asynchronous interface.
old-location: com\icallfactory_createcall.htm
tech.root: com
ms.assetid: 8df51aeb-4852-4dab-b1e9-e149ee115ea8
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CreateCall, CreateCall method [COM], CreateCall method [COM],ICallFactory interface, ICallFactory interface [COM],CreateCall method, ICallFactory.CreateCall, ICallFactory::CreateCall, _com_icallfactory_createcall, com.icallfactory_createcall, objidlbase/ICallFactory::CreateCall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - ICallFactory.CreateCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFactory::CreateCall


## -description


Creates an instance of the call object that corresponds to a specified asynchronous interface.


## -parameters




### -param riid [in]

A reference to the identifier for the asynchronous interface.


### -param pCtrlUnk [in]

A pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the call object. If this parameter is not <b>NULL</b>, the call object is aggregated in the specified object.
If this parameter is <b>NULL</b>, the call object is not aggregated.


### -param riid2 [in]

The identifier of an interface on the call object. Typical values are IID_IUnknown and IID_ISynchronize.


### -param ppv [out]

The address of a pointer to the interface specified by <i>riid2</i>. This parameter cannot be <b>NULL</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>riid</i> parameter does not reference the identifier for the asynchronous interface, such as IID_AsyncIEventSourceCallback.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/323dc627-3867-4170-b278-0bce46077729">ICallFactory</a>
 

 

