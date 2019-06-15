---
UID: NS:objidl.tagBIND_OPTS
title: BIND_OPTS (objidl.h)
author: windows-sdk-content
description: Contains parameters used during a moniker-binding operation.
old-location: com\bind_opts.htm
tech.root: com
ms.assetid: 764f09c9-ff20-4ae2-b94f-4b0a1e117e49
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPBIND_OPTS, BIND_OPTS, BIND_OPTS structure [COM], LPBIND_OPTS, LPBIND_OPTS structure pointer [COM], _com_BIND_OPTS, com.bind_opts, objidl/BIND_OPTS, objidl/LPBIND_OPTS"
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - BIND_OPTS
product: Windows
targetos: Windows
req.typenames: BIND_OPTS, *LPBIND_OPTS
req.redist: 
ms.custom: 19H1
---

# BIND_OPTS structure


## -description


Contains parameters used during a moniker-binding operation.

The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagbind_opts2">BIND_OPTS2</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagbind_opts3">BIND_OPTS3</a> structure can be used in place of the <b>BIND_OPTS</b> structure.


## -struct-fields




### -field cbStruct

The size of this structure, in bytes.


### -field grfFlags

Flags that control aspects of moniker binding operations. This value is any combination of the bit flags in the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-tagbind_flags">BIND_FLAGS</a> enumeration. The <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this member to zero.


### -field grfMode

Flags that should be used when opening the file that contains the object identified by the moniker. Possible values  are the <a href="https://docs.microsoft.com/windows/desktop/Stg/stgm-constants">STGM constants</a>. The binding operation uses these flags in the call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> when loading the file. If the object is already running, these flags are ignored by the binding operation. The <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this field to STGM_READWRITE. 


### -field dwTickCountDeadline

The clock time by which the caller would like the binding operation to be completed, in milliseconds. This member lets the caller limit the execution time of an operation when speed is of primary importance. A value of zero indicates that there is no deadline. Callers most often use this capability when calling the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a> method, though it can be usefully applied to other operations as well. The <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this field to zero.

Typical deadlines allow for a few hundred milliseconds of execution. This deadline is a recommendation, not a requirement; however, operations that exceed their deadline by a large amount may cause delays for the end user. Each moniker implementation should try to complete its operation by the deadline, or fail with the error MK_E_EXCEEDEDDEADLINE.

If a binding operation exceeds its deadline because one or more objects that it needs are not running, the moniker implementation should register the objects responsible in the bind context using the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a>. The objects should be registered under the parameter names "ExceededDeadline", "ExceededDeadline1", "ExceededDeadline2", and so on. If the caller later finds the object in the running object table, the caller can retry the binding operation.

The <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> function indicates the number of milliseconds since system startup, and wraps back to zero after 2^31 milliseconds. Consequently, callers should be careful not to inadvertently pass a zero value (which indicates no deadline), and moniker implementations should be aware of clock wrapping problems. 


## -remarks



A <b>BIND_OPTS</b> structure is stored in a bind context; the same bind context is used by each component of a composite moniker during binding, allowing the same parameters to be passed to all components of a composite moniker. See <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> for more information about bind contexts.

Moniker clients (use a moniker to acquire an interface pointer to an object) typically do not need to specify values for the members of this structure. The <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function creates a bind context with the bind options set to default values that are suitable for most situations; the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-bindmoniker">BindMoniker</a> function does the same thing when creating a bind context for use in binding a moniker. If you want to modify the values of these bind options, you can do so by passing a <b>BIND_OPTS</b> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">IBindCtx::SetBindOptions</a> method. Moniker implementers can pass a <b>BIND_OPTS</b> structure to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getbindoptions">IBindCtx::GetBindOptions</a> method to retrieve the values of these bind options.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
 

 

