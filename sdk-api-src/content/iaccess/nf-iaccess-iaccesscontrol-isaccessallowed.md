---
UID: NF:iaccess.IAccessControl.IsAccessAllowed
title: IAccessControl::IsAccessAllowed (iaccess.h)
description: Determines whether the specified trustee has access rights to the object or property.
helpviewer_keywords: ["IAccessControl interface [COM]","IsAccessAllowed method","IAccessControl.IsAccessAllowed","IAccessControl::IsAccessAllowed","IsAccessAllowed","IsAccessAllowed method [COM]","IsAccessAllowed method [COM]","IAccessControl interface","_com_iaccesscontrol_isaccessallowed","com.iaccesscontrol_isaccessallowed","iaccess/IAccessControl::IsAccessAllowed"]
old-location: com\iaccesscontrol_isaccessallowed.htm
tech.root: com
ms.assetid: ee9e7e2d-caec-443c-937d-b8fc64130ad4
ms.date: 12/05/2018
ms.keywords: IAccessControl interface [COM],IsAccessAllowed method, IAccessControl.IsAccessAllowed, IAccessControl::IsAccessAllowed, IsAccessAllowed, IsAccessAllowed method [COM], IsAccessAllowed method [COM],IAccessControl interface, _com_iaccesscontrol_isaccessallowed, com.iaccesscontrol_isaccessallowed, iaccess/IAccessControl::IsAccessAllowed
req.header: iaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
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
 - IAccessControl::IsAccessAllowed
 - iaccess/IAccessControl::IsAccessAllowed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IAccess.h
api_name:
 - IAccessControl.IsAccessAllowed
---

# IAccessControl::IsAccessAllowed


## -description

Determines whether the specified trustee has access rights to the object or property.

## -parameters

### -param pTrustee [in]

A pointer to a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

### -param lpProperty [in]

The name of the property. If you are using the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this parameter must be <b>NULL</b>.

### -param AccessRights [in]

The access rights on the object. If you are using the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this value must be either 0 or 1 (COM_RIGHTS_EXECUTE).

### -param pfAccessAllowed [out]

Indicates whether access is allowed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In the system-supplied implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a> (CLSID_DCOMAccessControl), <b>IsAccessAllowed</b> can be called only during a distributed COM call, and the only valid trustee name is the name of the client.

The following tables list the object-specific access permissions used with the Directory Service and storage implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>.

The following permissions are specific to DS objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_DS_OPEN
</td>
<td>Open a DS object
</td>
</tr>
<tr>
<td>ACTRL_DS_CREATE_CHILD
</td>
<td>Create a child object
</td>
</tr>
<tr>
<td>ACTRL_DS_DELETE_CHILD
</td>
<td>Delete a child object</td>
</tr>
<tr>
<td>ACTRL_DS_LIST
</td>
<td>Enumerate an object</td>
</tr>
<tr>
<td>ACTRL_DS_SELF
</td>
<td>Update a member list involving the trustee</td>
</tr>
<tr>
<td>ACTRL_DS_READ_PROP
</td>
<td>Read properties</td>
</tr>
<tr>
<td>ACTRL_DS_WRITE_PROP
</td>
<td>Write properties</td>
</tr>
</table>
 

The following permissions are specific to file objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_FILE_READ</td>
<td>Read from a file</td>
</tr>
<tr>
<td>ACTRL_FILE_WRITE</td>
<td>Write to a file</td>
</tr>
<tr>
<td>ACTRL_FILE_APPEND</td>
<td>Append to a file</td>
</tr>
<tr>
<td>ACTRL_FILE_READ_PROP</td>
<td>Read file properties or extended attributes</td>
</tr>
<tr>
<td>ACTRL_FILE_WRITE_PROP</td>
<td>Write file properties or extended attributes</td>
</tr>
<tr>
<td>ACTRL_FILE_EXECUTE</td>
<td>Execute the file</td>
</tr>
<tr>
<td>ACTRL_FILE_READ_ATTRIB</td>
<td>Read the file attributes</td>
</tr>
<tr>
<td>ACTRL_FILE_WRITE_ATTRIB
</td>
<td>Write the file attributes</td>
</tr>
</table>
 

The following permissions are specific to directory objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_DIR_LIST</td>
<td>List the contents of a directory</td>
</tr>
<tr>
<td>ACTRL_DIR_CREATE_OBJECT
</td>
<td>Create a child object (file) in a directory</td>
</tr>
<tr>
<td>ACTRL_DIR_CREATE_CHILD</td>
<td>Create a subdirectory</td>
</tr>
<tr>
<td>ACTRL_DIR_DELETE_CHILD</td>
<td>Delete a subdirectory</td>
</tr>
<tr>
<td>ACTRL_DIR_TRAVERSE
</td>
<td>Traverse the directory</td>
</tr>
</table>
 

The following permissions are specific to kernel objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_KERNEL_TERMINATE</td>
<td>Terminate a process or thread</td>
</tr>
<tr>
<td>ACTRL_KERNEL_THREAD</td>
<td>Create a thread</td>
</tr>
<tr>
<td>ACTRL_KERNEL_VM</td>
<td>Perform address space operations</td>
</tr>
<tr>
<td>ACTRL_KERNEL_VM_READ</td>
<td>Read from memory</td>
</tr>
<tr>
<td>ACTRL_KERNEL_VM_WRITE</td>
<td>Write to memory</td>
</tr>
<tr>
<td>ACTRL_KERNEL_DUP_HANDLE
</td>
<td>Duplicate a handle</td>
</tr>
<tr>
<td>ACTRL_KERNEL_PROCESS</td>
<td>Create a process</td>
</tr>
<tr>
<td>ACTRL_KERNEL_SET_INFO</td>
<td>Get kernel object information or state</td>
</tr>
<tr>
<td>ACTRL_KERNEL_GET_INFO</td>
<td>Set kernel object information or state</td>
</tr>
<tr>
<td>ACTRL_KERNEL_CONTROL</td>
<td>Control a kernel object (such as suspending a thread)</td>
</tr>
<tr>
<td>ACTRL_KERNEL_ALERT</td>
<td>Alert a kernel object.</td>
</tr>
<tr>
<td>ACTRL_KERNEL_GET_CONTEXT</td>
<td>Get the thread context</td>
</tr>
<tr>
<td>ACTRL_KERNEL_SET_CONTEXT</td>
<td>Set the thread context</td>
</tr>
<tr>
<td>ACTRL_KERNEL_TOKEN</td>
<td>Set the thread token</td>
</tr>
<tr>
<td>ACTRL_KERNEL_IMPERSONATE</td>
<td>Impersonate a client</td>
</tr>
<tr>
<td>ACTRL_KERNEL_DIMPERSONATE
</td>
<td>Directly impersonate a client</td>
</tr>
</table>
 

The following permissions are specific to printer objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_PRINT_SADMIN</td>
<td>Administer a print server</td>
</tr>
<tr>
<td>ACTRL_PRINT_SLIST</td>
<td>Enumerate a print server</td>
</tr>
<tr>
<td>ACTRL_PRINT_PADMIN</td>
<td>Administer a printer</td>
</tr>
<tr>
<td>ACTRL_PRINT_PUSE</td>
<td>Use a printer</td>
</tr>
<tr>
<td>ACTRL_PRINT_JADMIN</td>
<td>Administer a print job</td>
</tr>
</table>
 

The following permissions are specific to service objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_SVC_GET_INFO</td>
<td>Start a service</td>
</tr>
<tr>
<td>ACTRL_SVC_SET_INFO</td>
<td>Stop a service</td>
</tr>
<tr>
<td>ACTRL_SVC_STATUS</td>
<td>Pause a service</td>
</tr>
<tr>
<td>ACTRL_SVC_LIST</td>
<td>Enumerate the services</td>
</tr>
<tr>
<td>ACTRL_SVC_START</td>
<td>Start a service</td>
</tr>
<tr>
<td>ACTRL_SVC_STOP</td>
<td>Stop a service</td>
</tr>
<tr>
<td>ACTRL_SVC_PAUSE</td>
<td>Pause a service</td>
</tr>
<tr>
<td>ACTRL_SVC_INTERROGATE</td>
<td>Query the service for current status</td>
</tr>
<tr>
<td>ACTRL_SVC_UCONTROL</td>
<td>User-defined control </td>
</tr>
</table>
 

The following permissions are specific to registry objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_REG_QUERY</td>
<td>Read a registry subkey</td>
</tr>
<tr>
<td>ACTRL_REG_SET</td>
<td>Write a registry subkey</td>
</tr>
<tr>
<td>ACTRL_REG_CREATE_CHILD</td>
<td>Create a registry subkey</td>
</tr>
<tr>
<td>ACTRL_REG_LIST</td>
<td>Enumerate a registry subkey</td>
</tr>
<tr>
<td>ACTRL_REG_NOTIFY</td>
<td>Create a registry notification</td>
</tr>
<tr>
<td>ACTRL_REG_LINK
</td>
<td>Create a symbolic link</td>
</tr>
</table>
 

The following permissions are specific to window objects.

<table>
<tr>
<th>Access permission</th>
<th>Description</th>
</tr>
<tr>
<td>ACTRL_WIN_CLIPBRD</td>
<td>Enable access to the clipboard</td>
</tr>
<tr>
<td>ACTRL_WIN_GLOBAL_ATOMS</td>
<td>Enable global-atom access</td>
</tr>
<tr>
<td>ACTRL_WIN_CREATE</td>
<td>Create desktop access</td>
</tr>
<tr>
<td>ACTRL_WIN_LIST_DESK</td>
<td>Enumerate the desktops</td>
</tr>
<tr>
<td>ACTRL_WIN_LIST</td>
<td>Enumerate the window station</td>
</tr>
<tr>
<td>ACTRL_WIN_READ_ATTRIBS</td>
<td>Read the attributes</td>
</tr>
<tr>
<td>ACTRL_WIN_WRITE_ATTRIBS</td>
<td>Write the attributes</td>
</tr>
<tr>
<td>ACTRL_WIN_SCREEN</td>
<td>Enable access to the screen</td>
</tr>
<tr>
<td>ACTRL_WIN_EXIT</td>
<td>Call <a href="/windows/desktop/api/winuser/nf-winuser-exitwindows">ExitWindows</a> or <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>