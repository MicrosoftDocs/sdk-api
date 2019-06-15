---
UID: NF:msiquery.MsiSummaryInfoSetPropertyA
title: MsiSummaryInfoSetPropertyA function (msiquery.h)
author: windows-sdk-content
description: The MsiSummaryInfoSetProperty function sets a single summary information property.
old-location: setup\msisummaryinfosetproperty.htm
tech.root: Msi
ms.assetid: 0cd04068-537e-497a-97ff-7aea4e316b87
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiSummaryInfoSetProperty, MsiSummaryInfoSetProperty function, MsiSummaryInfoSetPropertyA, MsiSummaryInfoSetPropertyW, _msi_msisummaryinfosetproperty, msiquery/MsiSummaryInfoSetProperty, msiquery/MsiSummaryInfoSetPropertyA, msiquery/MsiSummaryInfoSetPropertyW, setup.msisummaryinfosetproperty
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiSummaryInfoSetPropertyA function


## -description


The 
<b>MsiSummaryInfoSetProperty</b> function sets a single summary information property.


<div class="alert"><b>Note</b>  The meaning of the property value depends on whether the summary information stream is for an installation database (.msi file), transform (.mst file) or patch (.msp file). See <a href="https://docs.microsoft.com/windows/desktop/Msi/summary-property-descriptions">Summary Property Descriptions</a> and <a href="https://docs.microsoft.com/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a> for more information about summary information properties.</div>
<div> </div>



## -parameters




### -param hSummaryInfo [in]

Handle to summary information.


### -param uiProperty [in]

Specifies the property ID of the summary property being set. This parameter can be a property ID  listed in the <a href="https://docs.microsoft.com/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.  This function does not set values for PID_DICTIONARY OR PID_THUMBNAIL property.


### -param uiDataType [in]

Specifies the type of property to set. This parameter can be a type listed in the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/summaryinfo-summaryinfo">Summaryinfo.Property</a>
 

 

