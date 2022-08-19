---
UID: NF:objidl.ICallFactory.CreateCall
title: ICallFactory::CreateCall (objidl.h)
description: The ICallFactory::CreateCall method (objidl.h) creates an instance of the call object that corresponds to a specified asynchronous interface.
helpviewer_keywords: ["CreateCall","CreateCall method [COM]","CreateCall method [COM]","ICallFactory interface","ICallFactory interface [COM]","CreateCall method","ICallFactory.CreateCall","ICallFactory::CreateCall","_com_icallfactory_createcall","com.icallfactory_createcall","objidlbase/ICallFactory::CreateCall"]
old-location: com\icallfactory_createcall.htm
tech.root: com
ms.assetid: 8df51aeb-4852-4dab-b1e9-e149ee115ea8
ms.date: 08/12/2022
ms.keywords: CreateCall, CreateCall method [COM], CreateCall method [COM],ICallFactory interface, ICallFactory interface [COM],CreateCall method, ICallFactory.CreateCall, ICallFactory::CreateCall, _com_icallfactory_createcall, com.icallfactory_createcall, objidlbase/ICallFactory::CreateCall
req.header: objidl.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICallFactory::CreateCall
 - objidl/ICallFactory::CreateCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ICallFactory.CreateCall
---

# ICallFactory::CreateCall


## -description

Creates an instance of the call object that corresponds to a specified asynchronous interface.

## -parameters

### -param riid [in]

A reference to the identifier for the asynchronous interface.

### -param pCtrlUnk [in]

A pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the call object. If this parameter is not <b>NULL</b>, the call object is aggregated in the specified object, and the <i>riid2</i> parameter must be IID_IUnknown.
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

<a href="/windows/desktop/api/objidl/nn-objidl-icallfactory">ICallFactory</a>
