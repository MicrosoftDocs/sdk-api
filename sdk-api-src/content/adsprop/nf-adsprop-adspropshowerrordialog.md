---
UID: NF:adsprop.ADsPropShowErrorDialog
title: ADsPropShowErrorDialog function
author: windows-sdk-content
description: The ADsPropShowErrorDialog function displays a dialog box that contains the error messages accumulated through calls to the ADsPropSendErrorMessage function or the WM_ADSPROP_NOTIFY_ERROR.
old-location: ad\adspropshowerrordialog.htm
tech.root: ad
ms.assetid: c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ADsPropShowErrorDialog, ADsPropShowErrorDialog function [Active Directory], ad.adspropshowerrordialog, adsprop/ADsPropShowErrorDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: adsprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsprop.dll
api_name:
 - ADsPropShowErrorDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ADsPropShowErrorDialog function


## -description


The <b>ADsPropShowErrorDialog</b> function displays a dialog box that contains the error messages accumulated through calls to the <a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a> function or the <a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>.


## -parameters




### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


### -param hPage [in]

The window handle of the property page.


## -returns



Returns zero if the notification object does not exist or nonzero otherwise.




## -remarks



The error messages added by the <a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a> function are accumulated until  <b>ADsPropShowErrorDialog</b> is called.  <b>ADsPropShowErrorDialog</b> combines and displays the accumulated  error messages. When the error dialog is dismissed, the accumulated error messages are deleted.




## -see-also




<a href="https://msdn.microsoft.com/584cb3e7-3b26-4346-9162-b3e3064ded1a">ADSPROPERROR</a>



<a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a>



<a href="https://msdn.microsoft.com/32a4724b-3182-4521-975c-cef33afee0b2">Messages in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>
 

 

