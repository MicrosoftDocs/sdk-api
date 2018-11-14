---
UID: NF:dvbsiparser.IISDB_EMM.Initialize
title: IISDB_EMM::Initialize
author: windows-sdk-content
description: Initializes the data elements of an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table by using the list of MPEG-2 EMM sections.
old-location: mstv\iisdb_emm_initialize.htm
tech.root: MSTV
ms.assetid: 127e7987-6782-4577-9104-86124d948d18
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IISDB_EMM interface [Microsoft TV Technologies],Initialize method, IISDB_EMM.Initialize, IISDB_EMM::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_EMM interface, dvbsiparser/IISDB_EMM::Initialize, mstv.iisdb_emm_initialize
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
 - IISDB_EMM.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IISDB_EMM.Initialize
: 
---

# IISDB_EMM::Initialize


## -description


Initializes the data elements of  an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table
   by using the
  list of MPEG-2 EMM sections.



## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface for the
MPEG-2 ISDB EMM section list.


### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1389e7c-a3f1-4782-b811-5e09615b3e47">IISDB_EMM</a>



<a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a>



<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a>
 

 

