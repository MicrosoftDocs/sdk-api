---
UID: NF:dvbsiparser.IISDB_EMM.GetIndividualEmmMessage
title: IISDB_EMM::GetIndividualEmmMessage (dvbsiparser.h)
author: windows-sdk-content
description: Gets an individual message from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
old-location: mstv\iisdb_emm_getindividualemmmessage.htm
tech.root: mstv
ms.assetid: 311b4efb-dacb-41e1-a798-913e3f99b168
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIndividualEmmMessage, GetIndividualEmmMessage method [Microsoft TV Technologies], GetIndividualEmmMessage method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetIndividualEmmMessage method, IISDB_EMM.GetIndividualEmmMessage, IISDB_EMM::GetIndividualEmmMessage, dvbsiparser/IISDB_EMM::GetIndividualEmmMessage, mstv.iisdb_emm_getindividualemmmessage
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IISDB_EMM.GetIndividualEmmMessage"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_EMM.GetIndividualEmmMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_EMM::GetIndividualEmmMessage


## -description


Gets an individual message from an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.
  


## -parameters




### -param pUnknown [in]

Pointer to the <b>IUnknown</b> interface for the object that contains the EMM table.


### -param pwLength [out]

Receives the length of the buffer required to hold the message.


### -param ppbMessage [out]

Pointer to a memory block allocated to receive the message object.
  The caller is responsible for freeing this memory.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>
 

 

