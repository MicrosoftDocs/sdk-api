---
UID: NS:objidl.tagBIND_OPTS3
title: tagBIND_OPTS3
author: windows-sdk-content
description: Contains parameters used during a moniker-binding operation.
old-location: com\bind_opts3.htm
tech.root: com
ms.assetid: 7e668313-229a-4d04-b8a2-d5072c87a5b5
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: "*LPBIND_OPTS3, BIND_OPTS3, BIND_OPTS3 structure [COM], LPBIND_OPTS3, LPBIND_OPTS3 structure pointer [COM], _com_BIND_OPTS3, com.bind_opts3, objidl/BIND_OPTS3, objidl/LPBIND_OPTS3, tagBIND_OPTS3"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - BIND_OPTS3
product: Windows
targetos: Windows
req.typenames: BIND_OPTS3, *LPBIND_OPTS3
req.redist: 
---

# tagBIND_OPTS3 structure


## -description


Contains parameters used during a moniker-binding operation.


## -struct-fields




### -field hwnd

A handle to the window that becomes the owner of the elevation UI, if applicable. If <b>hwnd</b> is <b>NULL</b>, COM will call the <a href="_win32_GetActiveWindow_cpp">GetActiveWindow</a> function to find a window handle associated with the current thread. This case might occur if the client is a script, which cannot fill in a <b>BIND_OPTS3</b> structure. In this case, COM will try to use the window associated with the script thread.



### -field tagBIND_OPTS2

 




#### - cbStruct

The size of this structure, in bytes.


#### - dwClassContext

The class context, taken from the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration, that is to be used for instantiating the object. Monikers typically pass this value to the <i>dwClsContext</i> parameter of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>.


#### - dwTickCountDeadline

The clock time by which the caller would like the binding operation to be completed, in milliseconds. This member lets the caller limit the execution time of an operation when speed is of primary importance. A value of zero indicates that there is no deadline. Callers most often use this capability when calling the <a href="https://msdn.microsoft.com/120cc951-6797-4ef6-890b-57ff8d3d23ba">IMoniker::GetTimeOfLastChange</a> method, though it can be usefully applied to other operations as well. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this field to zero.

Typical deadlines allow for a few hundred milliseconds of execution. This deadline is a recommendation, not a requirement; however, operations that exceed their deadline by a large amount may cause delays for the end user. Each moniker implementation should try to complete its operation by the deadline, or fail with the error MK_E_EXCEEDEDDEADLINE.

If a binding operation exceeds its deadline because one or more objects that it needs are not running, the moniker implementation should register the objects responsible in the bind context using the <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a>. The objects should be registered under the parameter names "ExceededDeadline", "ExceededDeadline1", "ExceededDeadline2", and so on. If the caller later finds the object in the running object table, the caller can retry the binding operation.

The <a href="https://msdn.microsoft.com/22201c82-a49a-4972-9f49-6baf6d23a1ea">GetTickCount</a> function indicates the number of milliseconds since system startup, and wraps back to zero after 2^31 milliseconds. Consequently, callers should be careful not to inadvertently pass a zero value (which indicates no deadline), and moniker implementations should be aware of clock wrapping problems. 


#### - dwTrackFlags

A moniker can use this value during link tracking. If the original persisted data that the moniker is referencing has been moved, the moniker can attempt to reestablish the link by searching for the original data though some adequate mechanism. This member provides additional information on how the link should be resolved. See the documentation of the <i>fFlags</i> parameter in <a href="_win32_IShellLink_Resolve">IShellLink::Resolve</a>.

COM's file moniker implementation uses the shell link mechanism to reestablish links and passes these flags to <a href="_win32_IShellLink_Resolve">IShellLink::Resolve</a>. 


#### - grfFlags

Flags that control aspects of moniker binding operations. This value is any combination of the bit flags in the <a href="https://msdn.microsoft.com/e8884e82-5de2-4a1f-b79c-d431afe9e87e">BIND_FLAGS</a> enumeration. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this member to zero.


#### - grfMode

Flags that should be used when opening the file that contains the object identified by the moniker. Possible values  are the <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM constants</a>. The binding operation uses these flags in the call to <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a> when loading the file. If the object is already running, these flags are ignored by the binding operation. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function initializes this field to STGM_READWRITE. 


#### - locale

The <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">LCID value</a> indicating the client's preference for the locale to be used by the object to which they are binding. A moniker passes this value to <a href="https://msdn.microsoft.com/1bbffe63-bd3a-40c8-aece-63121a437269">IClassActivator::GetClassObject</a>.


#### - pServerInfo

A pointer to a <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a> structure. This member allows clients calling <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> to specify server information. Clients may pass a <a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a> structure to the <a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">IBindCtx::SetBindOptions</a> method. If a server name is specified in the <b>COSERVERINFO</b> structure, the moniker bind will be forwarded to the specified computer. <b>SetBindOptions</b> only copies the struct members of <b>BIND_OPTS2</b>, not the <b>COSERVERINFO</b> structure and the pointers it contains. Callers may not free any of these pointers until the bind context is released. COM's new class moniker does not currently honor the <b>pServerInfo</b> flag.



## -remarks



A <b>BIND_OPTS3</b> structure is stored in a bind context; the same bind context is used by each component of a composite moniker during binding, allowing the same parameters to be passed to all components of a composite moniker. See <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> for more information about bind contexts.

Moniker clients (use a moniker to acquire an interface pointer to an object) typically do not need to specify values for the members of this structure. The <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function creates a bind context with the bind options set to default values that are suitable for most situations; the <a href="https://msdn.microsoft.com/5a022c39-fc2c-458b-9dfe-fed1255d49a4">BindMoniker</a> function does the same thing when creating a bind context for use in binding a moniker. If you want to modify the values of these bind options, you can do so by passing a <b>BIND_OPTS3</b> structure to the <a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">IBindCtx::SetBindOptions</a> method. Moniker implementers can pass a <b>BIND_OPTS3</b> structure to the <a href="https://msdn.microsoft.com/ccb239ee-922f-4e66-8aca-7651c0243a2b">IBindCtx::GetBindOptions</a> method to retrieve the values of these bind options.




## -see-also




<a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a>



<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

