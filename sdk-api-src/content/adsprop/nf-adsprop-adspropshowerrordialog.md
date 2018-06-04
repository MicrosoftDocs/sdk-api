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

# ADsPropShowErrorDialog function


## -description


The <b>ADsPropShowErrorDialog</b> function displays a dialog box that contains the error messages accumulated through calls to the <a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a> function or the <a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>.


## -parameters




### -param hNotifyObj

TBD


### -param hPage [in]

The window handle of the property page.


#### - hNotifyObject [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


## -returns



Returns zero if the notification object does not exist or nonzero otherwise.




## -remarks



The error messages added by the <a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a> function are accumulated until  <b>ADsPropShowErrorDialog</b> is called.  <b>ADsPropShowErrorDialog</b> combines and displays the accumulated  error messages. When the error dialog is dismissed, the accumulated error messages are deleted.




## -see-also




<a href="https://msdn.microsoft.com/584cb3e7-3b26-4346-9162-b3e3064ded1a">ADSPROPERROR</a>



<a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a>



<a href="https://msdn.microsoft.com/32a4724b-3182-4521-975c-cef33afee0b2">Messages in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>
 

 

