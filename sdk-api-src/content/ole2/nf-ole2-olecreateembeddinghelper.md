---
UID: NF:ole2.OleCreateEmbeddingHelper
title: OleCreateEmbeddingHelper function (ole2.h)
description: Creates an OLE embedding helper object using application-supplied code aggregated with pieces of the OLE default object handler. This helper object can be created and used in a specific context and role, as determined by the caller.
helpviewer_keywords: ["OleCreateEmbeddingHelper","OleCreateEmbeddingHelper function [COM]","_ole_OleCreateEmbeddingHelper","com.olecreateembeddinghelper","ole2/OleCreateEmbeddingHelper"]
old-location: com\olecreateembeddinghelper.htm
tech.root: com
ms.assetid: 5c67b513-0692-4e0a-beab-8b514089699c
ms.date: 12/05/2018
ms.keywords: OleCreateEmbeddingHelper, OleCreateEmbeddingHelper function [COM], _ole_OleCreateEmbeddingHelper, com.olecreateembeddinghelper, ole2/OleCreateEmbeddingHelper
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleCreateEmbeddingHelper
 - ole2/OleCreateEmbeddingHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - OleCreateEmbeddingHelper
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# OleCreateEmbeddingHelper function


## -description

Creates an OLE embedding helper object using application-supplied code aggregated with pieces of the OLE default object handler. This helper object can be created and used in a specific context and role, as determined by the caller.

## -parameters

### -param clsid [in]

CLSID of the class to be helped.

### -param pUnkOuter [in]

If the embedding helper is to be aggregated, pointer to the outer object's controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. If it is not to be aggregated, although this is rare, the value should be <b>NULL</b>.

### -param flags [in]

DWORD containing flags that specify the role and creation context for the embedding helper. For legal values, see the following Remarks section.

### -param pCF [in]

Pointer to the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface on the class object the function uses to create the secondary object. In some situations, this value may be <b>NULL</b>. For more information, see the following Remarks section.

### -param riid [in]

Reference to the identifier of the interface desired by the caller.

### -param lplpObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created embedding helper.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provided interface identifier is invalid.

</td>
</tr>
</table>

## -remarks

The <b>OleCreateEmbeddingHelper</b> function creates an object that supports the same interface implementations found in the default handler, but which has additional hooks that allow it to be used more generally than just as a handler object. The following two calls produce the same result: 




``` syntax
OleCreateEmbeddingHelper(clsid, pUnkOuter, EMBDHLP_INPROC_HANDLER | 
    EMBDHLP_CREATENOW, NULL, iid, ppvObj) 
 
OleCreateDefaultHandler(clsid, pUnkOuter, iid, ppvObj) 
```

The embedding helper is aggregatable; <i>pUnkOuter</i> is the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the aggregate of which the embedding helper is to be a part. It is used to create a new instance of the OLE default handler, which can be used to support objects in various roles. The caller passes a pointer to its <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> implementation to <b>OleCreateEmbeddingHelper</b>. This object and the default handler are then aggregated to create the new embedding helper object.



The <b>OleCreateEmbeddingHelper</b> function is usually used to support one of the following implementations: 



<ul>
<li>
An EXE object application that is being used as both a container and a server, and which supports inserting objects into itself. For this case, <b>CreateEmbeddingHelper</b> allows the object to support the interfaces usually supported only in the handler. To accomplish this, the application must first register its CLSID for different contexts, making two registration calls to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> function, rather than one, as follows: 


``` syntax
CoRegisterClassObject(clsidMe, pUnkCfLocal, CLSCTX_LOCAL_SERVER, 
        REGCLS_MULTI_SEPARATE...) 
 
    CoRegisterClassObject(clsidMe, pUnkCfInProc, CLSCTX_INPROC_SERVER, 
    
        REGCLS_MULTI_SEPARATE...) 
```

In these calls, you would pass along different class factory implementations to each of <i>pUnkCfLocal</i> and <i>pUnkCfInProc</i>. The class factory pointed to by <i>pUnkCfLocal</i> would be used to create objects that are to be embedded in a remote process, which is the normal case which uses a handler object associated with the client. However, when a server both creates an object and embeds it within itself, <i>pUnkCfInProc</i> points to a class object that can create an object that supports the handler interfaces. The local class is used to create the object and the in-process class creates the embedding helper, passing in the pointer to the first object's class factory in <i>pCF</i>. 


</li>
<li>
A custom in-process object handler, in which case, the DLL creates the embedding helper by passing in a pointer to a private implementation of <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> in <i>pCF</i>.


</li>
</ul>
The flags parameter indicates how the embedding helper is to be used and how and when the embedding helper is initialized. The values for flags are obtained by OR-ing together values from the following table.

<table>
<tr>
<th>Values for <i>flags</i> Parameter</th>
<th>Purpose</th>
</tr>
<tr>
<td>
EMBDHLP_INPROC_HANDLER

</td>
<td>
Creates an embedding helper that can be used with DLL object applications; specifically, the helper exposes the caching features of the default object handler.


</td>
</tr>
<tr>
<td>
EMBDHLP_INPROC_SERVER

</td>
<td>
Creates an embedding helper that is to be used as part of an in-process server. <i>pCF</i> cannot be <b>NULL</b>.


</td>
</tr>
<tr>
<td>
EMBDHLP_CREATENOW

</td>
<td>
Creates the secondary object using <i>pCF</i> immediately; if pCF is <b>NULL</b>, the standard proxy manager is used.


</td>
</tr>
<tr>
<td>
EMBDHLP_DELAYCREATE

</td>
<td>
Delays creation of the secondary object until it is needed (when the helper is put into the running state) to enhance speed and memory use. <i>pCF</i> must not be <b>NULL</b>. The EMBDHLP_INPROC_HANDLER flag cannot be used with this flag.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatedefaulthandler">OleCreateDefaultHandler</a>
