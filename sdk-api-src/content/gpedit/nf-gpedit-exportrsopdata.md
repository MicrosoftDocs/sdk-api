---
UID: NF:gpedit.ExportRSoPData
title: ExportRSoPData function
author: windows-driver-content
description: The ExportRSoPData function exports a WMI namespace that contains RSoP information to a data file. The function writes the information to a data file that can be imported to a WMI namespace with a call to the ImportRSoPData function.
old-location: policy\exportrsopdata.htm
old-project: Policy
ms.assetid: a3f20a35-8d9c-403b-ba76-24c8b3640c6d
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: ExportRSoPData, ExportRSoPData function [Group Policy], _win32_exportrsopdata, gpedit/ExportRSoPData, policy.exportrsopdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Gpedit.dll
api_name:
-	ExportRSoPData
product: Windows
targetos: Windows
req.lib: Gpedit.lib
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# ExportRSoPData function


## -description


The
    <b>ExportRSoPData</b> function exports a WMI namespace that contains RSoP information to a data file. The function writes the information to a data file that can be imported to a WMI namespace with a call to the 
<a href="https://msdn.microsoft.com/d3b4ef2e-a828-445a-83de-d5c9e4a4d98b">ImportRSoPData</a> function.


## -parameters




### -param lpNameSpace [in]

A pointer to a string that specifies the namespace which contains the RSoP data.


### -param lpFileName [in]

A pointer to a string that specifies the name of the file to receive the RSoP data.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.




## -remarks



It is recommended that you call the 
<b>ExportRSoPData</b> function twice: one time to process the user data and a second time to process the computer data.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/d3b4ef2e-a828-445a-83de-d5c9e4a4d98b">ImportRSoPData</a>
 

 

