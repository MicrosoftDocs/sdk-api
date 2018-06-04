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

# _ADSPROPERROR structure


## -description


The
  <b>ADSPROPERROR</b> structure is used to pass error
  data to the notification object with the <a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a> function or the <a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a> message.


## -struct-fields




### -field hwndPage

Contains the window handle of the property page that generated the error.


### -field pszPageTitle

Pointer to a NULL-terminated Unicode string that contains the title of the property page that generated the error.


### -field pszObjPath

Pointer to a NULL-terminated Unicode string that contains the ADsPath of the directory object that the error occurred on.


### -field pszObjClass

Pointer to a NULL-terminated Unicode string that contains the class name of the directory object that the error occurred on.


### -field hr

Contains an <b>HRESULT</b> value that specifies the  code of the error that occurred. If <i>hr</i> is not equal to <b>S_OK</b>, then <i>pszError</i> is ignored. If <i>hr</i>
    is equal to <b>S_OK</b>, then <i>pszError</i> contains an error message.


### -field pszError

Pointer to a NULL-terminated Unicode string that contains the error message to be displayed in the error dialog box. This member is ignored if <i>hr</i> is not equal to <b>S_OK</b>. In this case, the error dialog box will display a system-defined message for the error specified by <i>hr</i>.


## -see-also




<a href="https://msdn.microsoft.com/a1ca8440-0b18-4439-9143-bd8119f4f6ae">ADsPropSendErrorMessage</a>



<a href="https://msdn.microsoft.com/7abf1b3d-5abe-42cd-baeb-1bf863c7f04d">WM_ADSPROP_NOTIFY_ERROR</a>
 

 

