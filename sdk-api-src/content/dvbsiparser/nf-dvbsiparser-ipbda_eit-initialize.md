---
UID: NF:dvbsiparser.IPBDA_EIT.Initialize
title: IPBDA_EIT::Initialize (dvbsiparser.h)
author: windows-sdk-content
description: Initializes an object that gets data from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbda_eit_initialize.htm
tech.root: mstv
ms.assetid: 1f0d5a6e-eaa8-4694-b6d6-f1217ec6eb88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPBDA_EIT interface [Microsoft TV Technologies],Initialize method, IPBDA_EIT.Initialize, IPBDA_EIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPBDA_EIT interface, dvbsiparser/IPBDA_EIT::Initialize, mstv.ipbda_eit_initialize
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPBDA_EIT.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_EIT::Initialize


## -description


Initializes an object that gets data from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.  This method is called internally by the <a href="https://msdn.microsoft.com/ab7df40a-6a1c-4017-bece-618fb75797cf">IPBDASiParser::GetEIT</a> method, so applications typically should not call it.


## -parameters




### -param size [in]

Specifies the buffer size for data used to initialize each section.


### -param pBuffer [in]

Specifies the buffer used to initialize each section.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56">IPBDA_EIT</a>
 

 

