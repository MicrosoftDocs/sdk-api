---
UID: NF:tapi3if.ITLegacyAddressMediaControl2.ConfigDialog
title: ITLegacyAddressMediaControl2::ConfigDialog (tapi3if.h)
author: windows-sdk-content
description: The ConfigDialog method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device. The parameters that can be edited are those currently in use on the device.
old-location: tapi3\itlegacyaddressmediacontrol2_configdialog.htm
tech.root: Tapi
ms.assetid: ac2f7afe-4531-454a-8696-ca21556a049a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ConfigDialog, ConfigDialog method [TAPI 2.2], ConfigDialog method [TAPI 2.2],ITLegacyAddressMediaControl2 interface, ITLegacyAddressMediaControl2 interface [TAPI 2.2],ConfigDialog method, ITLegacyAddressMediaControl2.ConfigDialog, ITLegacyAddressMediaControl2::ConfigDialog, _tapi3_itlegacyaddressmediacontrol2_configdialog, tapi3.itlegacyaddressmediacontrol2_configdialog, tapi3if/ITLegacyAddressMediaControl2::ConfigDialog
ms.topic: method
f1_keywords: 
 - "tapi3if/ITLegacyAddressMediaControl2.ConfigDialog"
dev_langs:
 - c++
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
 - ITLegacyAddressMediaControl2.ConfigDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyAddressMediaControl2::ConfigDialog


## -description


The 
<b>ConfigDialog</b> method causes the provider of the specified line device to display a dialog box to allow the user to configure parameters related to the line device. The parameters that can be edited are those currently in use on the device.


## -parameters




### -param hwndOwner [in]

A handle to a window to which the dialog box is to be attached. This parameter can be <b>NULL</b> to indicate that a window created by the method should have no owner window.


### -param pDeviceClass [in]

Pointer to a <b>BSTR</b> that specifies a device class name. This device class allows the application to select a specific subscreen of configuration information applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest-level configuration is selected.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method translates to a TAPI 2.<i>x</i>
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> function call. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol2-configdialogedit">ITLegacyAddressMediaControl2::ConfigDialogEdit</a> method translates to a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a> call. These methods differ in their source of parameters to edit and the result of the editing on an active connection. For a discussion about these differences, see 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineconfigdialogedit">lineConfigDialogEdit</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2">ITLegacyAddressMediaControl2</a>
 

 

