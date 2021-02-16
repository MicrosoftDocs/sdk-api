---
UID: NF:comsvcs.ISharedPropertyGroupManager.CreatePropertyGroup
title: ISharedPropertyGroupManager::CreatePropertyGroup (comsvcs.h)
description: Creates a new shared property group.
helpviewer_keywords: ["CreatePropertyGroup","CreatePropertyGroup method [COM+]","CreatePropertyGroup method [COM+]","ISharedPropertyGroupManager interface","ISharedPropertyGroupManager interface [COM+]","CreatePropertyGroup method","ISharedPropertyGroupManager.CreatePropertyGroup","ISharedPropertyGroupManager::CreatePropertyGroup","_cos_ISharedPropertyGroupManager_CreatePropertyGroup","comsvcs/ISharedPropertyGroupManager::CreatePropertyGroup","cos.isharedpropertygroupmanager_createpropertygroup"]
old-location: cos\isharedpropertygroupmanager_createpropertygroup.htm
tech.root: cos
ms.assetid: 19c954cb-1a3b-4063-a09b-54906ae1613d
ms.date: 12/05/2018
ms.keywords: CreatePropertyGroup, CreatePropertyGroup method [COM+], CreatePropertyGroup method [COM+],ISharedPropertyGroupManager interface, ISharedPropertyGroupManager interface [COM+],CreatePropertyGroup method, ISharedPropertyGroupManager.CreatePropertyGroup, ISharedPropertyGroupManager::CreatePropertyGroup, _cos_ISharedPropertyGroupManager_CreatePropertyGroup, comsvcs/ISharedPropertyGroupManager::CreatePropertyGroup, cos.isharedpropertygroupmanager_createpropertygroup
req.header: comsvcs.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISharedPropertyGroupManager::CreatePropertyGroup
 - comsvcs/ISharedPropertyGroupManager::CreatePropertyGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroupManager.CreatePropertyGroup
---

# ISharedPropertyGroupManager::CreatePropertyGroup


## -description

Creates a new shared property group. If a property group with the specified name already exists, <b>CreatePropertyGroup</b> returns a reference to the existing group.

## -parameters

### -param Name [in]

The name of the shared property group to be created.

### -param dwIsoMode [in, out]

The isolation mode for the properties in the new shared property group. See the table of constants in Remarks below. If the value of the <i>fExists</i> parameter is set to VARIANT_TRUE on return from this method, the input value is ignored and the value returned in this parameter is the isolation mode that was assigned when the property group was created.

### -param dwRelMode [in, out]

The release mode for the properties in the new shared property group. See the table of constants in Remarks below. If the value of the <i>fExists</i> parameter is set to VARIANT_TRUE on return from this method, the input value is ignored and the value returned in this parameter is the release mode that was assigned when the property group was created.

### -param fExists [out]

VARIANT_TRUE on return from this method if the shared property group specified in the name parameter existed prior to this call, and VARIANT_FALSE if the property group was created by this call.

### -param ppGroup [out]

A reference to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroup">ISharedPropertyGroup</a>, which is a shared property group identified by the <i>Name</i> parameter, or <b>NULL</b> if an error is encountered.

## -returns

This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
A reference to the shared property group specified in the <i>Name</i> parameter is returned in the <i>ppGroup</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONTEXT_E_NOCONTEXT </b></dt>
</dl>
</td>
<td width="60%">
The caller is not executing under COM+. A caller must be executing under COM+ to use the Shared Property Manager.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG 
</b></dt>
</dl>
</td>
<td width="60%">
At least one of the parameters is not valid, or the same object is attempting to create the same property group more than once.

</td>
</tr>
</table>

## -remarks

The following constants are used to specify the effective isolation mode for a shared property group.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>LockSetGet
</td>
<td>0</td>
<td>The default value. It assures that every get or set operation on a shared property is atomic by locking the property during the call. This ensures that two clients cannot read or write to the same property at the same time, but it does not prevent other clients from concurrently accessing other properties in the same group.
</td>
</tr>
<tr>
<td>LockMethod
</td>
<td>1</td>
<td>This value locks all the properties in the shared property group for exclusive use by the caller as long as the caller's current method is executing. This is the appropriate mode to use when there are interdependencies among properties, or in cases where a client may have to update a property immediately after reading it before it can be accessed again.
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  When you set the isolation mode to LockMethod, the Shared Property Manager requires access to the calling object's object context. You cannot use this isolation mode to create a shared property group from within an object's constructor or from a non-COM+ object because the object context is not available during object construction and a base client does not have an object context.</div>
<div> </div>
The following constants are used to specify the effective release mode for a shared property group.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>Standard
</td>
<td>0</td>
<td>The default value. When all clients have released their references on the property group, the property group is automatically destroyed.
</td>
</tr>
<tr>
<td>Process
</td>
<td>1</td>
<td>The property group is not destroyed until the process in which it was created has terminated. Objects that hold references on a property group must still call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on their references.
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  An object should never attempt to pass a shared property group reference to another object. If the reference is passed outside of the object that acquired it, it is no longer a valid reference.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroupmanager">ISharedPropertyGroupManager</a>