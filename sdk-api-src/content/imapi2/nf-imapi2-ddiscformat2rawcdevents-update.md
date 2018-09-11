---
UID: NF:imapi2.DDiscFormat2RawCDEvents.Update
title: DDiscFormat2RawCDEvents::Update
author: windows-sdk-content
description: Implement this method to receive progress notification of the current raw-image write operation.
old-location: imapi\ddiscformat2rawcdevents_update.htm
tech.root: imapi
ms.assetid: abe35eee-63a4-4109-8927-825f86b6e302
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DDiscFormat2RawCDEvents interface [IMAPI],Update method, DDiscFormat2RawCDEvents.Update, DDiscFormat2RawCDEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DDiscFormat2RawCDEvents interface, imapi.ddiscformat2rawcdevents_update, imapi2/DDiscFormat2RawCDEvents::Update
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - DDiscFormat2RawCDEvents.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

