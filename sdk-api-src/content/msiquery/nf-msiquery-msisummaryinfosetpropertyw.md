---
UID: NF:msiquery.MsiSummaryInfoSetPropertyW
title: MsiSummaryInfoSetPropertyW function
author: windows-sdk-content
description: The MsiSummaryInfoSetProperty function sets a single summary information property.
old-location: setup\msisummaryinfosetproperty.htm
old-project: Msi
ms.assetid: 0cd04068-537e-497a-97ff-7aea4e316b87
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiSummaryInfoSetProperty, MsiSummaryInfoSetProperty function, MsiSummaryInfoSetPropertyA, MsiSummaryInfoSetPropertyW, _msi_msisummaryinfosetproperty, msiquery/MsiSummaryInfoSetProperty, msiquery/MsiSummaryInfoSetPropertyA, msiquery/MsiSummaryInfoSetPropertyW, setup.msisummaryinfosetproperty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiSummaryInfoSetProperty
-	MsiSummaryInfoSetPropertyA
-	MsiSummaryInfoSetPropertyW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSummaryInfoSetPropertyW function


## -description


The 
<b>MsiSummaryInfoSetProperty</b> function sets a single summary information property.


<div class="alert"><b>Note</b>  The meaning of the property value depends on whether the summary information stream is for an installation database (.msi file), transform (.mst file) or patch (.msp file). See <a href="https://msdn.microsoft.com/b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36">Summary Property Descriptions</a> and <a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a> for more information about summary information properties.</div>
<div> </div>



## -parameters




### -param hSummaryInfo [in]

Handle to summary information.


### -param uiProperty [in]

Specifies the property ID of the summary property being set. This parameter can be a property ID  listed in the <a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>.  This function does not set values for PID_DICTIONARY OR PID_THUMBNAIL property.


### -param uiDataType [in]

Specifies the type of property to set. This parameter can be a type listed in the 
<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>.


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




<a href="database_functions.htm">Summary Information Property Functions</a>



<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>



<a href="https://msdn.microsoft.com/8e8f0987-c92b-43f3-a61a-35099188c629">Summaryinfo.Property</a>
 

 

