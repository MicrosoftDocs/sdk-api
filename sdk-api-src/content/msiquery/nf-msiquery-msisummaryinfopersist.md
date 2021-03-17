---
UID: NF:msiquery.MsiSummaryInfoPersist
title: MsiSummaryInfoPersist function (msiquery.h)
description: The MsiSummaryInfoPersist function writes changed summary information back to the summary information stream.
helpviewer_keywords: ["MsiSummaryInfoPersist","MsiSummaryInfoPersist function","_msi_msisummaryinfopersist","msiquery/MsiSummaryInfoPersist","setup.msisummaryinfopersist"]
old-location: setup\msisummaryinfopersist.htm
tech.root: setup
ms.assetid: 76fd8339-2c57-4695-83c7-dcd3cd642f55
ms.date: 12/05/2018
ms.keywords: MsiSummaryInfoPersist, MsiSummaryInfoPersist function, _msi_msisummaryinfopersist, msiquery/MsiSummaryInfoPersist, setup.msisummaryinfopersist
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiSummaryInfoPersist
 - msiquery/MsiSummaryInfoPersist
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiSummaryInfoPersist
---

# MsiSummaryInfoPersist function


## -description

The 
<b>MsiSummaryInfoPersist</b> function writes changed summary information back to the summary information stream.

## -parameters

### -param hSummaryInfo [in]

Handle to summary information.

## -returns

This function returns UINT.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>