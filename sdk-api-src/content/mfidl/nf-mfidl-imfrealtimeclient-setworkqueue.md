---
UID: NF:mfidl.IMFRealTimeClient.SetWorkQueue
title: IMFRealTimeClient::SetWorkQueue
author: windows-driver-content
description: Specifies the work queue for the topology branch that contains this object.
old-location: mf\imfrealtimeclient_setworkqueue.htm
old-project: medfound
ms.assetid: 2744ddaf-a1ad-415a-b387-1a3d3b4821bf
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 2744ddaf-a1ad-415a-b387-1a3d3b4821bf, IMFRealTimeClient interface [Media Foundation],SetWorkQueue method, IMFRealTimeClient.SetWorkQueue, IMFRealTimeClient::SetWorkQueue, SetWorkQueue, SetWorkQueue method [Media Foundation], SetWorkQueue method [Media Foundation],IMFRealTimeClient interface, mf.imfrealtimeclient_setworkqueue, mfidl/IMFRealTimeClient::SetWorkQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFRealTimeClient.SetWorkQueue
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRealTimeClient::SetWorkQueue


## -description


Specifies the work queue for the topology branch that contains this object.


## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue, or the value <b>MFASYNC_CALLBACK_QUEUE_UNDEFINED</b>. See Remarks.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        An application can register a branch of the topology to use a private work queue. The Media Session notifies any pipeline object that supports <a href="https://msdn.microsoft.com/b1d1901e-dd49-421f-9212-61e32cff411e">IMFRealTimeClient</a> by calling <b>SetWorkQueue</b> with the application's work queue identifier.
      

When the application unregisters the topology branch, the Media Session calls <b>SetWorkQueue</b> again with the value <b>MFASYNC_CALLBACK_QUEUE_UNDEFINED</b>.
      




## -see-also




<a href="https://msdn.microsoft.com/b1d1901e-dd49-421f-9212-61e32cff411e">IMFRealTimeClient</a>



<a href="https://msdn.microsoft.com/62256ae8-a18a-4160-9f3f-a08ab3e93d6b">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a>
 

 

