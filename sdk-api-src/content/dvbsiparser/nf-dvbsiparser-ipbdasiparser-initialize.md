---
UID: NF:dvbsiparser.IPBDASiParser.Initialize
title: IPBDASiParser::Initialize (dvbsiparser.h)
description: Initializes a program and system information protocol (PSIP) parser for a Protected Broadcast Driver Architecture (PBDA) transport stream.
helpviewer_keywords: ["IPBDASiParser interface [Microsoft TV Technologies]","Initialize method","IPBDASiParser.Initialize","IPBDASiParser::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IPBDASiParser interface","dshow.ipbdasiparser_initialize","dvbsiparser/IPBDASiParser::Initialize","mstv.ipbdasiparser_initialize"]
old-location: mstv\ipbdasiparser_initialize.htm
tech.root: mstv
ms.assetid: fb161e1a-ae10-4d5e-907a-91c7e80c11d8
ms.date: 12/05/2018
ms.keywords: IPBDASiParser interface [Microsoft TV Technologies],Initialize method, IPBDASiParser.Initialize, IPBDASiParser::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPBDASiParser interface, dshow.ipbdasiparser_initialize, dvbsiparser/IPBDASiParser::Initialize, mstv.ipbdasiparser_initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPBDASiParser::Initialize
 - dvbsiparser/IPBDASiParser::Initialize
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
 - IPBDASiParser.Initialize
---

# IPBDASiParser::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Initializes a  program and system information protocol  (PSIP) parser for a Protected Broadcast Driver Architecture (PBDA) transport stream.

## -parameters

### -param punk [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the new object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdasiparser">IPBDASiParser</a>