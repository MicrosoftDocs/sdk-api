---
UID: NF:setupapi.SetupDiSetClassPropertyW
title: SetupDiSetClassPropertyW function
author: windows-sdk-content
description: The SetupDiSetClassProperty function sets a class property for a device setup class or a device interface class.
old-location: devinst\setupdisetclassproperty.htm
tech.root: devinst
ms.assetid: 12402336-9894-4d0d-b176-c6907e0cdcd4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupDiSetClassProperty, SetupDiSetClassProperty function [Device and Driver Installation], SetupDiSetClassPropertyA, SetupDiSetClassPropertyW, devinst.setupdisetclassproperty, di-rtns_c0346a11-5f87-4578-af46-5cb82e5b6101.xml, setupapi/SetupDiSetClassProperty, setupapi/SetupDiSetClassPropertyA, setupapi/SetupDiSetClassPropertyW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Set_Class_Property
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDiSetClassPropertyW (Unicode) and SetupDiSetClassPropertyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetClassProperty
 - SetupDiSetClassPropertyA
 - SetupDiSetClassPropertyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiSetClassPropertyW function


## -description


The <b>SetupDiSetClassProperty</b> function sets a class property for a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> or a <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a>.


## -parameters




### -param ClassGuid [in]

A pointer to a GUID that identifies the device setup class or device interface class for which to set a device property. For information about how to specify the class type, see the <i>Flags</i> parameter.


### -param PropertyKey [in]

A pointer to a <a href="https://msdn.microsoft.com/98986d43-84c0-44e6-83f9-08e872ea5e6d">DEVPROPKEY</a> structure that represents the device property key of the device class property to set.


### -param PropertyType [in]

A <a href="https://msdn.microsoft.com/e0fdcc28-be70-4ae1-bd6d-89e2177eae62">DEVPROPTYPE</a>-typed value that represents the property-data-type identifier for the device class property. For more information about the property-data-type identifier, see the <b>Remarks</b> section later in this topic.


### -param PropertyBuffer [in, optional]

A pointer to a buffer that contains the property value of the device class. If either the property or the data is being deleted, this pointer must be set to <b>NULL</b>, and <i>PropertyBufferSize</i> must be set to zero. For more information about property data, see the <b>Remarks</b> section later in this topic.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer</i> buffer. If <i>PropertyBuffer </i>is set to <b>NULL</b>, <i>PropertyBufferSize</i> must be set to zero.


### -param Flags [in]

One of the following values, which specifies whether the class is a device setup class or a device interface class:





#### DICLASSPROP_INSTALLER

<i>ClassGuid</i> specifies a device setup class. This flag cannot be used with DICLASSPROP_INTERFACE.



#### DICLASSPROP_INTERFACE

<i>ClassGuid</i> specifies a device interface class. This flag cannot be used with DICLASSPROP_INSTALLER.


## -returns



<b>SetupDiSetClassProperty</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b>, and the logged error can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.

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
The value of<i> Flags</i> is invalid. 

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
<dt><b>ERROR_INVALID_REFERENCE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The device interface reference string is not valid. This error can occur only if the DICLASSPROP_INTERFACE flag is specified. 

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
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
An unspecified internal data value was not valid. This error could be logged if the <i>ClassGuid</i> value is not a valid GUID or the property value is not consistent with the property type specified by <i>PropertyType.</i>

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
An unspecified item was not found. One possibility is that the property to be deleted does not exist. 

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



<b>SetupDiSetClassProperty</b> is part of the <a href="devinst.unified_device_property_model__windows_vista_and_later_">unified device property model</a>.

SetupAPI supports only a Unicode version of <b>SetupDiSetClassProperty</b>. 

A caller of <b>SetupDiSetClassProperty</b> must be a member of the Administrators group to set a device interface property. 

<b>SetupDiSetClassProperty</b> enforces requirements on the property-data-type identifier and the property value. 

To obtain the device property keys that represent the device properties that are set for a device class on a local computer, call <a href="https://msdn.microsoft.com/9b595fc5-f517-41f9-b7a8-a7811f658d57">SetupDiGetClassPropertyKeys</a>.

To retrieve a device class property on a local computer, call <a href="https://msdn.microsoft.com/b90473fe-eb8c-463a-971c-422c108dec1d">SetupDiGetClassProperty</a>, and to retrieve a device class property on a remote computer, call <a href="https://msdn.microsoft.com/74b6cd23-5741-4f0c-b5e1-6cdea2074c28">SetupDiGetClassPropertyEx</a>.

To set a device class property on a remote computer, call <a href="https://msdn.microsoft.com/99b58da2-0398-4dc1-8c9e-0eefaf03bf91">SetupDiSetClassPropertyEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/b90473fe-eb8c-463a-971c-422c108dec1d">SetupDiGetClassProperty</a>



<a href="https://msdn.microsoft.com/74b6cd23-5741-4f0c-b5e1-6cdea2074c28">SetupDiGetClassPropertyEx</a>



<a href="https://msdn.microsoft.com/9b595fc5-f517-41f9-b7a8-a7811f658d57">SetupDiGetClassPropertyKeys</a>



<a href="https://msdn.microsoft.com/99b58da2-0398-4dc1-8c9e-0eefaf03bf91">SetupDiSetClassPropertyEx</a>
 

 

