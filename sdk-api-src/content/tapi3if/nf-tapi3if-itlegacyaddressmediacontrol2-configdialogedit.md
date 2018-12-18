---
UID: NF:tapi3if.ITLegacyAddressMediaControl2.ConfigDialogEdit
title: ITLegacyAddressMediaControl2::ConfigDialogEdit
author: windows-sdk-content
description: The ConfigDialogEdit method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device.
old-location: tapi3\itlegacyaddressmediacontrol2_configdialogedit.htm
tech.root: tapi
ms.assetid: ff3e1cd4-bbd6-43c1-ad55-4787269821da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConfigDialogEdit, ConfigDialogEdit method [TAPI 2.2], ConfigDialogEdit method [TAPI 2.2],ITLegacyAddressMediaControl2 interface, ITLegacyAddressMediaControl2 interface [TAPI 2.2],ConfigDialogEdit method, ITLegacyAddressMediaControl2.ConfigDialogEdit, ITLegacyAddressMediaControl2::ConfigDialogEdit, _tapi3_itlegacyaddressmediacontrol2_configdialogedit, tapi3.itlegacyaddressmediacontrol2_configdialogedit, tapi3if/ITLegacyAddressMediaControl2::ConfigDialogEdit
ms.topic: method
req.header: tapi3if.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyAddressMediaControl2.ConfigDialogEdit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyAddressMediaControl2::ConfigDialogEdit


## -description


The 
<b>ConfigDialogEdit</b> method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device. The configuration data is passed in and out of this method by the application. (The data is the same as that retrieved by the 
<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">ITLegacyAddressMediaControl::GetDevConfig</a> method and set by the 
<a href="https://msdn.microsoft.com/7c5fe0ab-8a03-41db-994b-9786782cf7c1">ITLegacyAddressMediaControl::SetDevConfig</a> method.)


## -parameters




### -param hwndOwner [in]

A handle to a window to which the dialog box is to be attached. Can be <b>NULL</b> to indicate that a window created by the method should have no owner window.


### -param pDeviceClass [in]

Pointer to a <b>BSTR</b> that specifies a device class name. This device class allows the application to select a specific subscreen of configuration information applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest level configuration is selected.


### -param dwSizeIn [in]

Pointer to the size of the configuration data pointed to by the <i>pDeviceConfigIn</i> parameter.


### -param pDeviceConfigIn [in]

Pointer to an array of bytes containing device configuration data to edit.


### -param pdwSizeOut [out]

Pointer to the size of the configuration data pointed to by the <i>ppDeviceConfigOut</i> parameter.


### -param ppDeviceConfigOut [out]

Pointer to an array of bytes containing edited device configuration data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method translates to a TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/417016c3-8053-4a70-bce4-b96cce5e09a5">lineConfigDialogEdit</a> call. The 
<a href="https://msdn.microsoft.com/ac2f7afe-4531-454a-8696-ca21556a049a">ITLegacyAddressMediaControl2::ConfigDialog</a> method translates to a 
<a href="https://msdn.microsoft.com/52f23647-e9f5-48a3-95f4-1ac52898cb5a">lineConfigDialog</a> call. These methods differ in their source of parameters to edit and the result of the editing on an active connection. For a discussion about these differences, see 
<a href="https://msdn.microsoft.com/417016c3-8053-4a70-bce4-b96cce5e09a5">lineConfigDialogEdit</a>.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyAddressMediaControl2</a>



<a href="https://msdn.microsoft.com/ac2f7afe-4531-454a-8696-ca21556a049a">ITLegacyAddressMediaControl2::ConfigDialog</a>
 

 

