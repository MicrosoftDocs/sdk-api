---
UID: NF:mpeg2psiparser.IPSITables.GetTable
title: IPSITables::GetTable
author: windows-sdk-content
description: Gets an MPEG-2 Program Specific Information (PSI) table from an MPEG-2 transport stream. The table that is returned and its contents depend on the values of the three input parameters to this method.
old-location: mstv\ipsitables_gettable.htm
tech.root: mstv
ms.assetid: 4b2362c7-bfcb-40b8-813d-1a904149600e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTable, GetTable method [Microsoft TV Technologies], GetTable method [Microsoft TV Technologies],IPSITables interface, IPSITables interface [Microsoft TV Technologies],GetTable method, IPSITables.GetTable, IPSITables::GetTable, mpeg2psiparser/IPSITables::GetTable, mstv.ipsitables_gettable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: Mpeg2psiparser.idl
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
 - mpeg2psiparser.h
api_name:
 - IPSITables.GetTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mpeg2psiparser.h
: 
- IPSITables.GetTable
: 
---

# IPSITables::GetTable


## -description


Gets an MPEG-2 Program Specific Information (PSI) table from an MPEG-2 transport stream. The table that is returned and its contents depend on the values of the three input parameters to this method.


## -parameters




### -param dwTSID [in]

Transport stream identifier (TSID) for the table that is retrieved (bytes 0 - 15) and the original network ID (ONID) for an Event Information Table (EIT) that is retrieved (bytes 16 - 31).


### -param dwTID_PID [in]

Table identifier (TID) or the program ID (PID) that identifies the transport stream packet.


### -param dwHashedVer [in]

Hash value that identifies the table contents.


### -param dwPara4 [in]

PID for a Program Mapping Table or the service ID (SID) for an EIT. Otherwise, not used.


### -param ppIUnknown [out]

Pointer to  the <a href="iunknown">IUnknown</a> interface for the table object that is retrieved. The caller is responsible for freeing the memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a>



<a href="iunknown">IUnknown</a>
 

 

