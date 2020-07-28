---
UID: NF:dvbsiparser.IPBDA_Services.Initialize
title: IPBDA_Services::Initialize (dvbsiparser.h)
description: Initializes an object that retrieves service records from a Program and System Information Protocol (PSIP) table in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["IPBDA_Services interface [Microsoft TV Technologies]","Initialize method","IPBDA_Services.Initialize","IPBDA_Services::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IPBDA_Services interface","dvbsiparser/IPBDA_Services::Initialize","mstv.ipbda_services_initialize"]
old-location: mstv\ipbda_services_initialize.htm
tech.root: mstv
ms.assetid: 2504627a-a5e3-4ed1-9aa2-93d9621bf2e6
ms.date: 12/05/2018
ms.keywords: IPBDA_Services interface [Microsoft TV Technologies],Initialize method, IPBDA_Services.Initialize, IPBDA_Services::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPBDA_Services interface, dvbsiparser/IPBDA_Services::Initialize, mstv.ipbda_services_initialize
f1_keywords:
- dvbsiparser/IPBDA_Services.Initialize
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
- IPBDA_Services.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_Services::Initialize


## -description


Initializes an object that retrieves service records from a  Program and System Information Protocol (PSIP) table in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param size [in]

Specifies the size of the buffer used to initialize the object.


### -param pBuffer [in]

Pointer to the buffer containing the service data used for initialization.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_services">IPBDA_Services</a>
 

 

