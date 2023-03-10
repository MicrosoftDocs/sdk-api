---
UID: NS:objidl.tagBIND_OPTS3~r1
title: BIND_OPTS3
description: The BIND_OPTS3 structure contains parameters used during a moniker-binding operation.
ms.date: 08/13/2022
ms.keywords: tagBIND_OPTS3, BIND_OPTS3
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: objidl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: BIND_OPTS3, *LPBIND_OPTS3
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - tagBIND_OPTS3
 - objidl/tagBIND_OPTS3
 - LPBIND_OPTS3
 - objidl/LPBIND_OPTS3
 - BIND_OPTS3
 - objidl/BIND_OPTS3
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - objidl.h
api_name:
 - tagBIND_OPTS3
 - BIND_OPTS3
---

# BIND_OPTS3 structure


## -description

Contains parameters used during a moniker-binding operation.

## -struct-fields

### -field cbStruct

The size of this structure, in bytes.

### -field grfFlags

Flags that control aspects of moniker binding operations. This value is any combination of the bit flags in the <a href="/windows/desktop/api/objidl/ne-objidl-bind_flags">BIND_FLAGS</a> enumeration. The <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this member to zero.

### -field grfMode

Flags that should be used when opening the file that contains the object identified by the moniker. Possible values  are the <a href="/windows/desktop/Stg/stgm-constants">STGM constants</a>. The binding operation uses these flags in the call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> when loading the file. If the object is already running, these flags are ignored by the binding operation. The <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this field to STGM_READWRITE.

### -field dwTickCountDeadline

The clock time by which the caller would like the binding operation to be completed, in milliseconds. This member lets the caller limit the execution time of an operation when speed is of primary importance. A value of zero indicates that there is no deadline. Callers most often use this capability when calling the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-gettimeoflastchange">IMoniker::GetTimeOfLastChange</a> method, though it can be usefully applied to other operations as well. The <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function initializes this field to zero.

Typical deadlines allow for a few hundred milliseconds of execution. This deadline is a recommendation, not a requirement; however, operations that exceed their deadline by a large amount may cause delays for the end user. Each moniker implementation should try to complete its operation by the deadline, or fail with the error MK_E_EXCEEDEDDEADLINE.

If a binding operation exceeds its deadline because one or more objects that it needs are not running, the moniker implementation should register the objects responsible in the bind context using the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a>. The objects should be registered under the parameter names "ExceededDeadline", "ExceededDeadline1", "ExceededDeadline2", and so on. If the caller later finds the object in the running object table, the caller can retry the binding operation.

The <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> function indicates the number of milliseconds since system startup, and wraps back to zero after 2^31 milliseconds. Consequently, callers should be careful not to inadvertently pass a zero value (which indicates no deadline), and moniker implementations should be aware of clock wrapping problems.

### -field dwTrackFlags

A moniker can use this value during link tracking. If the original persisted data that the moniker is referencing has been moved, the moniker can attempt to reestablish the link by searching for the original data though some adequate mechanism. This member provides additional information on how the link should be resolved. See the documentation of the <i>fFlags</i> parameter in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve">IShellLink::Resolve</a>.

COM's file moniker implementation uses the shell link mechanism to reestablish links and passes these flags to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve">IShellLink::Resolve</a>.

### -field dwClassContext

The class context, taken from the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration, that is to be used for instantiating the object. Monikers typically pass this value to the <i>dwClsContext</i> parameter of <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>.

### -field locale

The <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">LCID value</a> indicating the client's preference for the locale to be used by the object to which they are binding. A moniker passes this value to <a href="/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject">IClassActivator::GetClassObject</a>.

### -field pServerInfo

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-coserverinfo">COSERVERINFO</a> structure. This member allows clients calling <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> to specify server information. Clients may pass a <a href="/windows/win32/api/objidl/ns-objidl-bind_opts2~r1">BIND_OPTS2</a> structure to the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">IBindCtx::SetBindOptions</a> method. If a server name is specified in the <b>COSERVERINFO</b> structure, the moniker bind will be forwarded to the specified computer. <b>SetBindOptions</b> only copies the struct members of <b>BIND_OPTS2</b>, not the <b>COSERVERINFO</b> structure and the pointers it contains. Callers may not free any of these pointers until the bind context is released. COM's new class moniker does not currently honor the <b>pServerInfo</b> flag.

### -field hwnd

A handle to the window that becomes the owner of the elevation UI, if applicable. If <b>hwnd</b> is <b>NULL</b>, COM will call the <a href="/windows/desktop/api/winuser/nf-winuser-getactivewindow">GetActiveWindow</a> function to find a window handle associated with the current thread. This case might occur if the client is a script, which cannot fill in a <b>BIND_OPTS3</b> structure. In this case, COM will try to use the window associated with the script thread.

## -remarks

A <b>BIND_OPTS3</b> structure is stored in a bind context; the same bind context is used by each component of a composite moniker during binding, allowing the same parameters to be passed to all components of a composite moniker. See <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> for more information about bind contexts.

Moniker clients (use a moniker to acquire an interface pointer to an object) typically do not need to specify values for the members of this structure. The <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> function creates a bind context with the bind options set to default values that are suitable for most situations; the <a href="/windows/desktop/api/objbase/nf-objbase-bindmoniker">BindMoniker</a> function does the same thing when creating a bind context for use in binding a moniker. If you want to modify the values of these bind options, you can do so by passing a <b>BIND_OPTS3</b> structure to the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">IBindCtx::SetBindOptions</a> method. Moniker implementers can pass a <b>BIND_OPTS3</b> structure to the <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getbindoptions">IBindCtx::GetBindOptions</a> method to retrieve the values of these bind options.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
