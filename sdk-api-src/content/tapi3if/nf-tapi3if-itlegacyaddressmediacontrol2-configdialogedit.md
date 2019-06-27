---
UID: NF:tapi3if.ITLegacyAddressMediaControl2.ConfigDialogEdit
title: ITLegacyAddressMediaControl2::ConfigDialogEdit (tapi3if.h)
author: windows-sdk-content
description: The ConfigDialogEdit method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device.
old-location: tapi3\itlegacyaddressmediacontrol2_configdialogedit.htm
tech.root: Tapi
ms.assetid: ff3e1cd4-bbd6-43c1-ad55-4787269821da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ConfigDialogEdit, ConfigDialogEdit method [TAPI 2.2], ConfigDialogEdit method [TAPI 2.2],ITLegacyAddressMediaControl2 interface, ITLegacyAddressMediaControl2 interface [TAPI 2.2],ConfigDialogEdit method, ITLegacyAddressMediaControl2.ConfigDialogEdit, ITLegacyAddressMediaControl2::ConfigDialogEdit, _tapi3_itlegacyaddressmediacontrol2_configdialogedit, tapi3.itlegacyaddressmediacontrol2_configdialogedit, tapi3if/ITLegacyAddressMediaControl2::ConfigDialogEdit
ms.topic: method
f1_keywords: 
 - "tapi3if/ITLegacyAddressMediaControl2.ConfigDialogEdit"
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
ms.custom: 19H1
---

# ITLegacyAddressMediaControl2::ConfigDialogEdit


## -description


The 
<b>ConfigDialogEdit</b> method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device. The configuration data is passed in and out of this method by the application. (The data is the same as that retrieved by the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">ITLegacyAddressMediaControl::GetDevConfig</a> method and set by the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-setdevconfig">ITLegacyAddressMediaControl::SetDevConfig</a> method.)


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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a> call. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol2-configdialog">ITLegacyAddressMediaControl2::ConfigDialog</a> method translates to a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> call. These methods differ in their source of parameters to edit and the result of the editing on an active connection. For a discussion about these differences, see 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyAddressMediaControl2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol2-configdialog">ITLegacyAddressMediaControl2::ConfigDialog</a>
 

 

