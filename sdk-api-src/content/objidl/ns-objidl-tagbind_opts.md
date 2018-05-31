---
UID: NS:objidl.tagBIND_OPTS
title: tagBIND_OPTS
author: windows-sdk-content
description: Contains parameters used during a moniker-binding operation.
old-location: com\bind_opts.htm
old-project: com
ms.assetid: 764f09c9-ff20-4ae2-b94f-4b0a1e117e49
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*LPBIND_OPTS, BIND_OPTS, BIND_OPTS structure [COM], LPBIND_OPTS, LPBIND_OPTS structure pointer [COM], _com_BIND_OPTS, com.bind_opts, objidl/BIND_OPTS, objidl/LPBIND_OPTS, tagBIND_OPTS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BIND_OPTS, *LPBIND_OPTS, LPBIND_OPTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Objidl.h
api_name:
-	BIND_OPTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagBIND_OPTS structure


## -description


Contains parameters used during a moniker-binding operation.

The <a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a> or <a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a> structure can be used in place of the <b>BIND_OPTS</b> structure.


## -struct-fields




### -field cbStruct

The size of this structure, in bytes.


### -field grfFlags

Flags that control aspects of moniker binding operations. This value is any combination of the bit flags in the <a href="https://msdn.microsoft.com/e8884e82-5de2-4a1f-b79c-d431afe9e87e">BIND_FLAGS</a> enumeration. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this member to zero.


### -field grfMode

Flags that should be used when opening the file that contains the object identified by the moniker. Possible values  are the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM constants</a>. The binding operation uses these flags in the call to <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a> when loading the file. If the object is already running, these flags are ignored by the binding operation. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this field to STGM_READWRITE. 


### -field dwTickCountDeadline

The clock time by which the caller would like the binding operation to be completed, in milliseconds. This member lets the caller limit the execution time of an operation when speed is of primary importance. A value of zero indicates that there is no deadline. Callers most often use this capability when calling the <a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">IMoniker::GetTimeOfLastChange</a> method, though it can be usefully applied to other operations as well. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this field to zero.

Typical deadlines allow for a few hundred milliseconds of execution. This deadline is a recommendation, not a requirement; however, operations that exceed their deadline by a large amount may cause delays for the end user. Each moniker implementation should try to complete its operation by the deadline, or fail with the error MK_E_EXCEEDEDDEADLINE.

If a binding operation exceeds its deadline because one or more objects that it needs are not running, the moniker implementation should register the objects responsible in the bind context using the <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a>. The objects should be registered under the parameter names "ExceededDeadline", "ExceededDeadline1", "ExceededDeadline2", and so on. If the caller later finds the object in the running object table, the caller can retry the binding operation.

The <a href="https://msdn.microsoft.com/22201c82-a49a-4972-9f49-6baf6d23a1ea">GetTickCount</a> function indicates the number of milliseconds since system startup, and wraps back to zero after 2^31 milliseconds. Consequently, callers should be careful not to inadvertently pass a zero value (which indicates no deadline), and moniker implementations should be aware of clock wrapping problems. 


## -remarks



A <b>BIND_OPTS</b> structure is stored in a bind context; the same bind context is used by each component of a composite moniker during binding, allowing the same parameters to be passed to all components of a composite moniker. See <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> for more information about bind contexts.

Moniker clients (use a moniker to acquire an interface pointer to an object) typically do not need to specify values for the members of this structure. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function creates a bind context with the bind options set to default values that are suitable for most situations; the <a href="https://msdn.microsoft.com/5a022c39-fc2c-458b-9dfe-fed1255d49a4">BindMoniker</a> function does the same thing when creating a bind context for use in binding a moniker. If you want to modify the values of these bind options, you can do so by passing a <b>BIND_OPTS</b> structure to the <a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">IBindCtx::SetBindOptions</a> method. Moniker implementers can pass a <b>BIND_OPTS</b> structure to the <a href="https://msdn.microsoft.com/ccb239ee-922f-4e66-8aca-7651c0243a2b">IBindCtx::GetBindOptions</a> method to retrieve the values of these bind options.




## -see-also




<a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a>



<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

