---
UID: NF:dvbsiparser.IPBDASiParser.GetServices
title: IPBDASiParser::GetServices (dvbsiparser.h)
description: Retrieves a list of services from the program and system information protocol (PSIP) tables in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetServices","GetServices method [Microsoft TV Technologies]","GetServices method [Microsoft TV Technologies]","IPBDASiParser interface","IPBDASiParser interface [Microsoft TV Technologies]","GetServices method","IPBDASiParser.GetServices","IPBDASiParser::GetServices","dshow.ipbdasiparser_getservices","dvbsiparser/IPBDASiParser::GetServices","mstv.ipbdasiparser_getservices"]
old-location: mstv\ipbdasiparser_getservices.htm
tech.root: mstv
ms.assetid: 0d6848f2-6fcd-4e7c-b1fc-b8f56e6c65b6
ms.date: 12/05/2018
ms.keywords: GetServices, GetServices method [Microsoft TV Technologies], GetServices method [Microsoft TV Technologies],IPBDASiParser interface, IPBDASiParser interface [Microsoft TV Technologies],GetServices method, IPBDASiParser.GetServices, IPBDASiParser::GetServices, dshow.ipbdasiparser_getservices, dvbsiparser/IPBDASiParser::GetServices, mstv.ipbdasiparser_getservices
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
 - IPBDASiParser::GetServices
 - dvbsiparser/IPBDASiParser::GetServices
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
 - IPBDASiParser.GetServices
---

# IPBDASiParser::GetServices


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Retrieves a list of services from the  program and system information protocol (PSIP) tables in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param dwSize [in]

Size of the buffer that receives the service list, in bytes.

### -param pBuffer [in]

Receives the buffer for services.

### -param ppServices [out]

Receives an <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_services">IPBDA_Services</a> interface pointer.  The caller must release this interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdasiparser">IPBDASiParser</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_services">IPBDA_Services</a>