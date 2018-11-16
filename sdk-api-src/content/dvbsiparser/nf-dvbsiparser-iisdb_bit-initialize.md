---
UID: NF:dvbsiparser.IISDB_BIT.Initialize
title: IISDB_BIT::Initialize
author: windows-sdk-content
description: Initializes the object by using captured table section data for an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_initialize.htm
tech.root: mstv
ms.assetid: 1c38cbc0-4e47-4f15-9a9b-548e74af6462
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IISDB_BIT interface [Microsoft TV Technologies],Initialize method, IISDB_BIT.Initialize, IISDB_BIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_BIT interface, dvbsiparser/IISDB_BIT::Initialize, mstv.iisdb_bit_initialize
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
 - IISDB_BIT.Initialize
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
- IISDB_BIT.Initialize
: 
---

# IISDB_BIT::Initialize


## -description


Initializes the object by using captured table section data
  for an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). 



## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface
  of the <b>SectionList</b> object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

