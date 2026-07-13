---
UID: NF:msiquery.MsiSummaryInfoSetPropertyA
title: MsiSummaryInfoSetPropertyA function (msiquery.h)
description: The MsiSummaryInfoSetProperty function sets a single summary information property. (ANSI)
helpviewer_keywords: ["MsiSummaryInfoSetPropertyA", "msiquery/MsiSummaryInfoSetPropertyA"]
old-location: setup\msisummaryinfosetproperty.htm
tech.root: setup
ms.assetid: 0cd04068-537e-497a-97ff-7aea4e316b87
ms.date: 12/05/2018
ms.keywords: MsiSummaryInfoSetProperty, MsiSummaryInfoSetProperty function, MsiSummaryInfoSetPropertyA, MsiSummaryInfoSetPropertyW, _msi_msisummaryinfosetproperty, msiquery/MsiSummaryInfoSetProperty, msiquery/MsiSummaryInfoSetPropertyA, msiquery/MsiSummaryInfoSetPropertyW, setup.msisummaryinfosetproperty
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSummaryInfoSetPropertyW (Unicode) and MsiSummaryInfoSetPropertyA (ANSI)
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
 - MsiSummaryInfoSetPropertyA
 - msiquery/MsiSummaryInfoSetPropertyA
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
 - MsiSummaryInfoSetProperty
 - MsiSummaryInfoSetPropertyA
 - MsiSummaryInfoSetPropertyW
---

# MsiSummaryInfoSetPropertyA function


## -description

The 
<b>MsiSummaryInfoSetProperty</b> function sets a single summary information property.


<div class="alert"><b>Note</b>  The meaning of the property value depends on whether the summary information stream is for an installation database (.msi file), transform (.mst file) or patch (.msp file). See <a href="/windows/desktop/Msi/summary-property-descriptions">Summary Property Descriptions</a> and <a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a> for more information about summary information properties.</div>
<div> </div>

## -parameters

### -param hSummaryInfo [in]

Handle to summary information.

### -param uiProperty [in]

Specifies the property ID of the summary property being set. This parameter can be a property ID  listed in the <a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.  This function does not set values for PID_DICTIONARY OR PID_THUMBNAIL property.

### -param uiDataType [in]

Specifies the type of property to set. This parameter can be a type listed in the 
<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.

### -param iValue [in]

Specifies the integer value.

### -param pftValue [in]

Specifies the file-time value.

### -param szValue [in]

Specifies the text value.

## -returns

The 
<b>MsiSummaryInfoSetProperty</b> function returns the following values:

## -see-also

<a href="/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>



<a href="/windows/desktop/Msi/summaryinfo-summaryinfo">Summaryinfo.Property</a>

## -remarks

> [!NOTE]
> The msiquery.h header defines MsiSummaryInfoSetProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
