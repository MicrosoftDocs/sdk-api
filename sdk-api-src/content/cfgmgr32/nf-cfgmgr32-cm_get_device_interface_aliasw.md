---
UID: NF:cfgmgr32.CM_Get_Device_Interface_AliasW
title: CM_Get_Device_Interface_AliasW function (cfgmgr32.h)
description: The CM_Get_Device_Interface_Alias function returns the alias of the specified device interface instance, if the alias exists. (Unicode)
helpviewer_keywords: ["CM_Get_Device_Interface_Alias", "CM_Get_Device_Interface_Alias function [Device and Driver Installation]", "CM_Get_Device_Interface_AliasW", "cfgmgr32/CM_Get_Device_Interface_Alias", "cfgmgr32/CM_Get_Device_Interface_AliasW", "cfgmgrfn_7650eacc-4b5e-4f88-81f2-a7f75462dfc1.xml", "devinst.cm_get_device_interface_alias"]
old-location: devinst\cm_get_device_interface_alias.htm
tech.root: devinst
ms.assetid: 855d1b3b-1c65-4a0d-a591-d9fbc235c4ca
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_Interface_Alias, CM_Get_Device_Interface_Alias function [Device and Driver Installation], CM_Get_Device_Interface_AliasW, cfgmgr32/CM_Get_Device_Interface_Alias, cfgmgr32/CM_Get_Device_Interface_AliasW, cfgmgrfn_7650eacc-4b5e-4f88-81f2-a7f75462dfc1.xml, devinst.cm_get_device_interface_alias
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_Interface_AliasW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Device_Interface_AliasW
 - cfgmgr32/CM_Get_Device_Interface_AliasW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
 - setupapi.dll
api_name:
 - CM_Get_Device_Interface_Alias
 - CM_Get_Device_Interface_AliasW
---

# CM_Get_Device_Interface_AliasW function


## -description

The <b>CM_Get_Device_Interface_Alias</b> function returns the alias of the specified device interface instance, if the alias exists.

## -parameters

### -param pszDeviceInterface [in]

Pointer to the name of the device interface instance for which to retrieve an alias. The caller typically received this string from a call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista">CM_Get_Device_Interface_List</a>, or in a PnP notification structure.

### -param AliasInterfaceGuid [in]

Pointer to a GUID specifying the interface class of the alias to retrieve.

### -param pszAliasDeviceInterface [out]

Specifies a pointer to a buffer, that upon successful return, points to a string containing the name of the alias. The caller must free this string when it is no longer needed.

A buffer is required.  Otherwise, the call will fail.

### -param pulLength [in, out]

Supplies the count of characters in <i>pszAliasDeviceInterface</i>          and receives the number of characters required to hold the alias device interface.

On input, this parameter must be greater than 0.

### -param ulFlags [in]

Reserved. Do not use.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_NO_SUCH_DEVICE_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
Possibly indicates that there is no alias of the specified interface class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_BUFFER_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed is too small.

</td>
</tr>
</table>

## -remarks

Device interfaces are considered aliases if they are exposed by the same underlying device and have identical interface reference strings, but are of different interface classes.

The <i>pszDeviceInterface</i> parameter specifies a device interface instance for a particular device, belonging to a particular interface class, with a particular reference string. <b>CM_Get_Device_Interface_Alias</b> returns another device interface instance for the same device and reference string, but of a different interface class, if it exists.

For example, the function driver for a fault-tolerant volume could register and set two device interfaces, one of the fault-tolerant-volume interface class and one of the volume interface class. Another driver could call <b>CM_Get_Device_Interface_Alias</b> with the symbolic link for one of the interfaces and ask whether the other interface exists by specifying its interface class.

Two device interfaces with <b>NULL</b> reference strings are aliases if they are exposed by the same underlying device and have different interface class GUIDs.
