---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.GetCommandOptions
title: IPortableDeviceCapabilities::GetCommandOptions (portabledeviceapi.h)
description: The GetCommandOptions method retrieves all the supported options for the specified command on the device.
helpviewer_keywords: ["GetCommandOptions","GetCommandOptions method [Windows Portable Devices SDK]","GetCommandOptions method [Windows Portable Devices SDK]","IPortableDeviceCapabilities interface","IPortableDeviceCapabilities interface [Windows Portable Devices SDK]","GetCommandOptions method","IPortableDeviceCapabilities.GetCommandOptions","IPortableDeviceCapabilities::GetCommandOptions","IPortableDeviceCapabilitiesGetCommandOptions","portabledeviceapi/IPortableDeviceCapabilities::GetCommandOptions","wpdsdk.iportabledevicecapabilities_getcommandoptions"]
old-location: wpdsdk\iportabledevicecapabilities_getcommandoptions.htm
tech.root: wpdsdk
ms.assetid: d222968f-3ca7-4a4d-bdc6-89a6ca98c7b0
ms.date: 12/05/2018
ms.keywords: GetCommandOptions, GetCommandOptions method [Windows Portable Devices SDK], GetCommandOptions method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],GetCommandOptions method, IPortableDeviceCapabilities.GetCommandOptions, IPortableDeviceCapabilities::GetCommandOptions, IPortableDeviceCapabilitiesGetCommandOptions, portabledeviceapi/IPortableDeviceCapabilities::GetCommandOptions, wpdsdk.iportabledevicecapabilities_getcommandoptions
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceCapabilities::GetCommandOptions
 - portabledeviceapi/IPortableDeviceCapabilities::GetCommandOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceCapabilities.GetCommandOptions
---

# IPortableDeviceCapabilities::GetCommandOptions


## -description

The <b>GetCommandOptions</b> method retrieves all the supported options for the specified command on the device.

## -parameters

### -param Command [in]

A <b>REFPROPERTYKEY</b> that specifies a command to query for supported options. For a list of the commands that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/commands">Commands</a>.

### -param ppOptions [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the supported options. If no options are supported, this will not contain any values. The caller must release this interface when it is done with it. For more information, see Remarks.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is called by applications that want to call a command directly on the driver by calling <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevice-sendcommand">IPortableDevice::SendCommand</a>. Some commands allow the caller to specify additional options. For example, some drivers support recursive child deletion when deleting an object using the WPD_COMMAND_OBJECT_MANAGEMENT_DELETE_OBJECTS command.
      

If an option is a simple Boolean value, the key of the retrieved <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface will be the name of the option, and the <b>PROPVARIANT</b> value will be a VT_BOOL value of True or False. If an option has several values, the retrieved <b>PROPVARIANT</b> value will be a collection type that holds the supported values.
      

If this method is called for the WPD_COMMAND_STORAGE_FORMAT command and the <i>ppOptions</i> parameter is set to WPD_OPTION_VALID_OBJECT_IDS, the driver will return an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariant</a> collection of type VT_LPWSTR that specifies the identifiers for each object on the device that can be formatted. (If this option does not exist, the format command is available for all objects.)

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities">IPortableDeviceCapabilities Interface</a>