---
UID: NF:setupapi.SetupDiGetClassPropertyW
title: SetupDiGetClassPropertyW function (setupapi.h)
description: The SetupDiGetClassProperty function retrieves a device property that is set for a device setup class or a device interface class.
helpviewer_keywords: ["SetupDiGetClassProperty","SetupDiGetClassProperty function [Device and Driver Installation]","SetupDiGetClassPropertyW","devinst.setupdigetclassproperty","di-rtns_0fff1c27-692b-488f-9cec-373e8f7b7484.xml","setupapi/SetupDiGetClassProperty"]
old-location: devinst\setupdigetclassproperty.htm
tech.root: devinst
ms.assetid: b90473fe-eb8c-463a-971c-422c108dec1d
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassProperty, SetupDiGetClassProperty function [Device and Driver Installation], SetupDiGetClassPropertyW, devinst.setupdigetclassproperty, di-rtns_0fff1c27-692b-488f-9cec-373e8f7b7484.xml, setupapi/SetupDiGetClassProperty
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_Class_Property
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassPropertyW
 - setupapi/SetupDiGetClassPropertyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetClassProperty
---

# SetupDiGetClassPropertyW function


## -description

The <b>SetupDiGetClassProperty</b> function retrieves a device property that is set for a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> or a <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>.

## -parameters

### -param ClassGuid [in]

A pointer to a GUID that identifies the device setup class or device interface class for which to retrieve a device property that is set for the device class. For information about specifying the class type, see the <i>Flags</i> parameter.

### -param PropertyKey [in]

A pointer to a <a href="/windows-hardware/drivers/install/devpropkey">DEVPROPKEY</a> structure that represents the device property key of the requested device class property.

### -param PropertyType [out]

A pointer to a <a href="/windows-hardware/drivers/install/property-data-type-identifiers">DEVPROPTYPE</a>-typed variable that receives the property-data-type identifier of the requested device class property, where the property-data-type identifier is the bitwise OR between a base-data-type identifier and, if the base data type is modified, a property-data-type modifier.

### -param PropertyBuffer [out]

A pointer to a buffer that receives the requested device class property. <b>SetupDiGetClassProperty</b> retrieves the requested property value only if the buffer is large enough to hold all the property value data. The pointer can be <b>NULL</b>. If the pointer is set to <b>NULL</b> and <i>RequiredSize</i> is supplied, <b>SetupDiGetClassProperty</b> returns the size of the device class property, in bytes, in *<i>RequiredSize</i>.

### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer</i> is set to <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.

### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives either the size, in bytes, of the device class property if the device class property is retrieved or the required buffer size if the buffer is not large enough. This pointer can be set to <b>NULL</b>.

### -param Flags [in]

One of the following values, which specifies whether the class is a device setup class or a device interface class.





#### DICLASSPROP_INSTALLER

<i>ClassGuid</i> specifies a device setup class. This flag cannot be used with DICLASSPROP_INTERFACE.



#### DICLASSPROP_INTERFACE

<i>ClassGuid</i> specifies a device interface class. This flag cannot be used with DICLASSPROP_INSTALLER.

## -returns

<b>SetupDiGetClassProperty</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

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
The value of<i> Flags</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The device setup class that is specified by <i>ClassGuid</i> is not valid. This error can occur only if the DICLASSPROP_INSTALLER flag is specified.

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
<dt><b>ERROR_INVALID_REG_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property key that is supplied by <i>PropertyKey</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_REFERENCE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The device interface reference string is not valid. This error can be returned if the DICLASSPROP_INTERFACE flag is specified. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An unspecified internal data value was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
A user buffer is not valid. One possibility is that <i>PropertyBuffer</i> is <b>NULL</b>, and <i>PropertyBufferSize</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The device interface class that is specified by <i>ClassGuid</i> does not exist. This error can occur only if the DICLASSPROP_INTERFACE flag is specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
An internal data buffer that was passed to a system call was too small.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested device property does not exist.

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

<b>SetupDiGetClassProperty</b> is part of the <a href="/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-">unified device property model</a>.

SetupAPI supports only a Unicode version of <b>SetupDiGetClassProperty</b>. 

A caller of <b>SetupDiGetClassProperty</b> must be a member of the Administrators group to set a device interface property. 

To obtain the device property keys that represent the device properties that are set for a device class on a local computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertykeys">SetupDiGetClassPropertyKeys</a>.

To retrieve a device class property on a remote computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertyexw">SetupDiGetClassPropertyEx</a>.

To set a device class property on a local computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a><b>,</b> and to set a device class property on a remote computer, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyexw">SetupDiSetClassPropertyEx</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertyexw">SetupDiGetClassPropertyEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclasspropertykeys">SetupDiGetClassPropertyKeys</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyw">SetupDiSetClassProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclasspropertyexw">SetupDiSetClassPropertyEx</a>