---
UID: NF:dvbsiparser.IPBDASiParser.GetEIT
title: IPBDASiParser::GetEIT
author: windows-sdk-content
description: Gets the event information table (EIT) from the program and system information protocol (PSIP) tables in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbdasiparser_geteit.htm
old-project: mstv
ms.assetid: ab7df40a-6a1c-4017-bece-618fb75797cf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEIT, GetEIT method [Microsoft TV Technologies], GetEIT method [Microsoft TV Technologies],IPBDASiParser interface, IPBDASiParser interface [Microsoft TV Technologies],GetEIT method, IPBDASiParser.GetEIT, IPBDASiParser::GetEIT, dshow.ipbdasiparser_geteit, dvbsiparser/IPBDASiParser::GetEIT, mstv.ipbdasiparser_geteit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
 - IPBDASiParser.GetEIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDASiParser::GetEIT


## -description


Gets the event information table (EIT) from  the program and system information protocol (PSIP) tables in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwSize [in]

Reserved. Set to zero.


### -param pBuffer [in]

Reserved. Set to <b>NULL</b>.


### -param ppEIT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56">IPBDA_EIT</a> interface.  The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1cc25ec-b519-4c24-ba85-f2c240749fbd">IPBDASiParser</a>
 

 

