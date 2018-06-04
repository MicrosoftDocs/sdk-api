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

# DDiscFormat2RawCDEvents::Update


## -description


Implement this method to receive progress notification of the current raw-image write operation. 


## -parameters




### -param object [in]

The <a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a> interface that initiated the write operation. 

This parameter is a <b>MsftDiscFormat2RawCD</b> object in script.


### -param progress [in]

An <a href="https://msdn.microsoft.com/b1988883-459c-46f1-a0d1-df9500a000e1">IDiscFormat2RawCDEventArgs</a> interface that you use to determine the progress of the write operation. 

This parameter is a <b>MsftDiscFormat2RawCD</b> object in script.


## -returns



Return values are ignored.




## -remarks



Notifications are sent in response to calling the <a href="https://msdn.microsoft.com/137395f1-b0cf-4bd0-9d3b-a21122eb8b57">IDiscFormat2RawCD::WriteMedia</a> or <a href="https://msdn.microsoft.com/636d04dd-081d-407c-827e-55e443516d9b">IDiscFormat2RawCD::WriteMedia2</a> method.

To stop the write process, call the <a href="https://msdn.microsoft.com/12cd6797-dcb8-496d-a141-9d3a805266e9">IDiscFormat2RawCD::CancelWrite</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3a06911e-8a50-4e41-874c-478ad05f6488">DDiscFormat2RawCDEvents</a>



<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/12cd6797-dcb8-496d-a141-9d3a805266e9">IDiscFormat2RawCD::CancelWrite</a>
 

 

