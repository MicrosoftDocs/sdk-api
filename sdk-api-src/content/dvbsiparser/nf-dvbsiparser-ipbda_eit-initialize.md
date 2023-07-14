---
UID: NF:dvbsiparser.IPBDA_EIT.Initialize
title: IPBDA_EIT::Initialize (dvbsiparser.h)
description: Initializes an object that gets data from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["IPBDA_EIT interface [Microsoft TV Technologies]","Initialize method","IPBDA_EIT.Initialize","IPBDA_EIT::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IPBDA_EIT interface","dvbsiparser/IPBDA_EIT::Initialize","mstv.ipbda_eit_initialize"]
old-location: mstv\ipbda_eit_initialize.htm
tech.root: mstv
ms.assetid: 1f0d5a6e-eaa8-4694-b6d6-f1217ec6eb88
ms.date: 12/05/2018
ms.keywords: IPBDA_EIT interface [Microsoft TV Technologies],Initialize method, IPBDA_EIT.Initialize, IPBDA_EIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPBDA_EIT interface, dvbsiparser/IPBDA_EIT::Initialize, mstv.ipbda_eit_initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPBDA_EIT::Initialize
 - dvbsiparser/IPBDA_EIT::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT.Initialize
---

# IPBDA_EIT::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Initializes an object that gets data from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.  This method is called internally by the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbdasiparser-geteit">IPBDASiParser::GetEIT</a> method, so applications typically should not call it.

## -parameters

### -param size [in]

Specifies the buffer size for data used to initialize each section.

### -param pBuffer [in]

Specifies the buffer used to initialize each section.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>