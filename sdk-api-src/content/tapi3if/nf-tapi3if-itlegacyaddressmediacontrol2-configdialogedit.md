---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

