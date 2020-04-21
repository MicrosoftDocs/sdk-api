---
UID: NF:msiquery.MsiSummaryInfoGetPropertyCount
title: MsiSummaryInfoGetPropertyCount function (msiquery.h)
description: The MsiSummaryInfoGetPropertyCount function returns the number of existing properties in the summary information stream.helpviewer_keywords: ["MsiSummaryInfoGetPropertyCount","MsiSummaryInfoGetPropertyCount function","_msi_msisummaryinfogetpropertycount","msiquery/MsiSummaryInfoGetPropertyCount","setup.msisummaryinfogetpropertycount"]
old-location: setup\msisummaryinfogetpropertycount.htm
tech.root: Msi
ms.assetid: 8a9fe9cc-8289-479a-acda-ce2a2b76705f
ms.date: 12/05/2018
ms.keywords: MsiSummaryInfoGetPropertyCount, MsiSummaryInfoGetPropertyCount function, _msi_msisummaryinfogetpropertycount, msiquery/MsiSummaryInfoGetPropertyCount, setup.msisummaryinfogetpropertycount
f1_keywords:
- msiquery/MsiSummaryInfoGetPropertyCount
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msi.dll
api_name:
- MsiSummaryInfoGetPropertyCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiSummaryInfoGetPropertyCount function


## -description


The 
<b>MsiSummaryInfoGetPropertyCount</b> function returns the number of existing properties in the summary information stream.


## -parameters




### -param hSummaryInfo [in]

Handle to summary information.


### -param puiPropertyCount [out]

Location to receive the total property count.


## -returns



This function returns UINT.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>
 

 

