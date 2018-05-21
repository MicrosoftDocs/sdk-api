---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetMessageControl
title: IIsdbCAServiceDescriptor::GetMessageControl
author: windows-driver-content
description: Gets the delay time, in days, before the automatic entitlement management message (EMM) is displayed from a conditional access (CA) service descriptor.
old-location: mstv\iisdbcaservicedescriptor_getmessagecontrol.htm
old-project: mstv
ms.assetid: 0a911c5e-a026-4d35-a6a2-e33ba53f3057
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetMessageControl, GetMessageControl method [Microsoft TV Technologies], GetMessageControl method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetMessageControl method, IIsdbCAServiceDescriptor.GetMessageControl, IIsdbCAServiceDescriptor::GetMessageControl, dvbsiparser/IIsdbCAServiceDescriptor::GetMessageControl, mstv.iisdbcaservicedescriptor_getmessagecontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbCAServiceDescriptor.GetMessageControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbCAServiceDescriptor::GetMessageControl


## -description


Gets the delay time, in days, before the automatic  entitlement management message (EMM) is displayed from a conditional access (CA) service descriptor.


## -parameters




### -param pbVal [out]

Receives the number of days before the EMM message is displayed. A value of 0xFF indicates that the delay time is
disabled (that the start of the delay time has been put on hold). 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When playing a previously received and stored program on a receiver with stored
reception functionality, a least significant bit of 1 in this field indicates that the
automatic display message will not be displayed.




## -see-also




<a href="https://msdn.microsoft.com/6d56e39d-3c7a-4c55-8d07-00e25eba18bd">IIsdbCAServiceDescriptor</a>
 

 

