---
UID: NF:mpeg2psiparser.IPSITables.GetTable
title: IPSITables::GetTable (mpeg2psiparser.h)
description: Gets an MPEG-2 Program Specific Information (PSI) table from an MPEG-2 transport stream. The table that is returned and its contents depend on the values of the three input parameters to this method.
helpviewer_keywords: ["GetTable","GetTable method [Microsoft TV Technologies]","GetTable method [Microsoft TV Technologies]","IPSITables interface","IPSITables interface [Microsoft TV Technologies]","GetTable method","IPSITables.GetTable","IPSITables::GetTable","mpeg2psiparser/IPSITables::GetTable","mstv.ipsitables_gettable"]
old-location: mstv\ipsitables_gettable.htm
tech.root: mstv
ms.assetid: 4b2362c7-bfcb-40b8-813d-1a904149600e
ms.date: 12/05/2018
ms.keywords: GetTable, GetTable method [Microsoft TV Technologies], GetTable method [Microsoft TV Technologies],IPSITables interface, IPSITables interface [Microsoft TV Technologies],GetTable method, IPSITables.GetTable, IPSITables::GetTable, mpeg2psiparser/IPSITables::GetTable, mstv.ipsitables_gettable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSITables::GetTable
 - mpeg2psiparser/IPSITables::GetTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mpeg2psiparser.h
api_name:
 - IPSITables.GetTable
---

# IPSITables::GetTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

Pointer to  the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the table object that is retrieved. The caller is responsible for freeing the memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>