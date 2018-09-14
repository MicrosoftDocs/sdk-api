---
UID: NF:msiquery.MsiSummaryInfoGetPropertyCount
title: MsiSummaryInfoGetPropertyCount function
author: windows-sdk-content
description: The MsiSummaryInfoGetPropertyCount function returns the number of existing properties in the summary information stream.
old-location: setup\msisummaryinfogetpropertycount.htm
tech.root: msi
ms.assetid: 8a9fe9cc-8289-479a-acda-ce2a2b76705f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MsiSummaryInfoGetPropertyCount, MsiSummaryInfoGetPropertyCount function, _msi_msisummaryinfogetpropertycount, msiquery/MsiSummaryInfoGetPropertyCount, setup.msisummaryinfogetpropertycount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="database_functions.htm">Summary Information Property Functions</a>



<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>
 

 

