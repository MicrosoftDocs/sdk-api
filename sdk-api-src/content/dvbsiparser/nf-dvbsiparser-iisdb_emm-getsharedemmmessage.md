---
UID: NF:dvbsiparser.IISDB_EMM.GetSharedEmmMessage
title: IISDB_EMM::GetSharedEmmMessage
author: windows-sdk-content
description: Gets a shared message from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
old-location: mstv\iisdb_emm_getsharedemmmessage.htm
old-project: mstv
ms.assetid: d3ad405c-cdf0-4a37-9495-3f126e6c0688
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSharedEmmMessage, GetSharedEmmMessage method [Microsoft TV Technologies], GetSharedEmmMessage method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetSharedEmmMessage method, IISDB_EMM.GetSharedEmmMessage, IISDB_EMM::GetSharedEmmMessage, dvbsiparser/IISDB_EMM::GetSharedEmmMessage, mstv.iisdb_emm_getsharedemmmessage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_EMM.GetSharedEmmMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_EMM::GetSharedEmmMessage


## -description


Gets a shared message from an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.
  


## -parameters




### -param pwLength [out]

Receives the length of the buffer required to hold the message.


### -param ppbMessage [out]

Pointer to a memory block allocated to receive the shared message object.
  The caller is responsible for freeing this memory.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1389e7c-a3f1-4782-b811-5e09615b3e47">IISDB_EMM</a>
 

 

