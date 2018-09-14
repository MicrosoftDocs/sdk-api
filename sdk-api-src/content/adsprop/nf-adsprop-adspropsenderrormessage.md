---
UID: NF:adsprop.ADsPropSendErrorMessage
title: ADsPropSendErrorMessage function
author: windows-sdk-content
description: The ADsPropSendErrorMessage function adds an error message to a list of error messages displayed by calling the ADsPropShowErrorDialog function.
old-location: ad\adspropsenderrormessage.htm
tech.root: ad
ms.assetid: a1ca8440-0b18-4439-9143-bd8119f4f6ae
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: ADsPropSendErrorMessage, ADsPropSendErrorMessage function [Active Directory], ad.adspropsenderrormessage, adsprop/ADsPropSendErrorMessage
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
 - ADsPropSendErrorMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ADsPropSendErrorMessage function


## -description


The <b>ADsPropSendErrorMessage</b> function adds an error message to a list of error messages displayed by calling 
the <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> function.


## -parameters




### -param hNotifyObj [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


### -param pError [out]

Pointer to an <a href="https://msdn.microsoft.com/584cb3e7-3b26-4346-9162-b3e3064ded1a">ADSPROPERROR</a> structure which contains data about the error message.


## -returns



Returns nonzero if successful or zero otherwise.




## -remarks



The error messages added by the <b>ADsPropSendErrorMessage</b> function are accumulated until  <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> is called.  <b>ADsPropShowErrorDialog</b> combines and displays the accumulated  error messages. When the error dialog is dismissed, the accumulated error messages are deleted.




## -see-also




<a href="https://msdn.microsoft.com/584cb3e7-3b26-4346-9162-b3e3064ded1a">ADSPROPERROR</a>



<a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a>



<a href="https://msdn.microsoft.com/32a4724b-3182-4521-975c-cef33afee0b2">Messages in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>
 

 

