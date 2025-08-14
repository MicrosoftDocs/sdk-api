---
UID: NF:setupapi.SetupDiGetClassPropertyKeys
title: SetupDiGetClassPropertyKeys function (setupapi.h)
description: The SetupDiGetClassPropertyKeys function retrieves an array of the device property keys that represent the device properties that are set for a device setup class or a device interface class.
helpviewer_keywords: ["SetupDiGetClassPropertyKeys","SetupDiGetClassPropertyKeys function [Device and Driver Installation]","devinst.setupdigetclasspropertykeys","di-rtns_7f87ef8b-8752-4cd4-9aca-811a83c99ccf.xml","setupapi/SetupDiGetClassPropertyKeys"]
old-location: devinst\setupdigetclasspropertykeys.htm
tech.root: devinst
ms.assetid: 9b595fc5-f517-41f9-b7a8-a7811f658d57
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassPropertyKeys, SetupDiGetClassPropertyKeys function [Device and Driver Installation], devinst.setupdigetclasspropertykeys, di-rtns_7f87ef8b-8752-4cd4-9aca-811a83c99ccf.xml, setupapi/SetupDiGetClassPropertyKeys
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_Class_Property_Keys
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassPropertyKeys
 - setupapi/SetupDiGetClassPropertyKeys
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.dll
api_name:
 - SetupDiGetClassPropertyKeys
---

# SetupDiGetClassPropertyKeys function


## -description

The <b>SetupDiGetClassPropertyKeys</b> function retrieves an array of the device property keys that represent the device properties that are set for a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> or a <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>.

## -parameters

### -param ClassGuid [in]

A pointer to a GUID that represents a device setup class or a device interface class. <b>SetupDiGetClassPropertyKeys</b> retrieves an array of the device property keys that represent device properties that are set for the specified class. For information about specifying the class type, see the <i>Flags</i> parameter.

### -param PropertyKeyArray [out, optional]

A pointer to a buffer that receives an array of <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a>-typed values, where each value is a device property key that represents a device property that is set for the device class. The pointer is optional and can be <b>NULL</b>. For more information, see the <b>Remarks</b> section later in this topic.

### -param PropertyKeyCount [in]

The size, in DEVPROPKEY-typed values, of the <i>PropertyKeyArray</i> buffer. If <i>PropertyKeyArray</i> is set to <b>NULL</b>, <i>PropertyKeyCount</i> must be set to zero.

### -param RequiredPropertyKeyCount [out, optional]

A pointer to a DWORD-typed variable that receives the number of requested property keys. The parameter is optional and can be set to <b>NULL</b>.

### -param Flags [in]

One of the following values, which specifies whether to retrieve property keys for a device setup class or for a device interface class:





#### DICLASSPROP_INSTALLER

<i>ClassGuid</i> specifies a device setup class. This flag cannot be used with DICLASSPROP_INTERFACE.



#### DICLASSPROP_INTERFACE

<i>ClassGuid</i> specifies a device interface class. This flag cannot be used with DICLASSPROP_INSTALLER.

## -returns

<b>SetupDiGetClassPropertyKeys</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table includes some of the more common error codes that this function might log.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value of<i> Flags</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_CLASS</b></dt>
</dl>
</td>
<td width="60%">
If the DICLASSPROP_INSTALLER flag is specified, this error code indicates that the device setup class that is specified by <i>ClassGuid</i> does not exist. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_REFERENCE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The reference string for the device interface that is specified by <i>ClassGuild</i> is not valid. This error can be returned if the DICLASSPROP_INTERFACE flag is specified. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An unspecified data value is not valid. One possibility is that the <i>ClassGuid</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An unspecified parameter is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyKeyArray</i> is <b>NULL</b>, and <i>PropertKeyCount</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE_CLASS</b></dt>
</dl>
</td>
<td width="60%">
If the DICLASSPROP_INTERFACE flag is specified, this error code indicates that the device interface class that is specified by <i>ClassGuid</i> does not exist. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>PropertyKeyArray</i> buffer is not large enough to hold all the property keys, or an internal data buffer that was passed to a system call was too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough system memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have Administrator privileges. 

</td>
</tr>
</table>

## -remarks

<b>SetupDiGetClassPropertyKeys</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">unified device property model</a>. 

A caller of <b>SetupDiGetClassPropertyKeys</b> must be a member of the Administrators group to retrieve device property keys for a device class. 

If the <i>PropertyKeyArray</i> buffer is not large enough to hold all the requested property keys, <b>SetupDiGetClassPropertyKeys</b> does not retrieve any property keys and returns ERROR_INSUFFICIENT_BUFFER. If the caller supplied a <i>RequiredPropertyKeyCount</i> pointer, <b>SetupDiGetClassPropertyKeys</b> sets the value of *<i>RequiredPropertyKeyCount</i> to the required size, in DEVPROPKEY-typed values, of the <i>PropertyKeyArray </i> buffer<i>.</i>

To retrieve a device class property on a local computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertyw">SetupDiGetClassProperty</a>. To set a device class property on a local computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a>.

To retrieve the property keys for a device setup class or device interface class on a remote computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertykeysexw">SetupDiGetClassPropertyKeysEx</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertyw">SetupDiGetClassProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertykeysexw">SetupDiGetClassPropertyKeysEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a>