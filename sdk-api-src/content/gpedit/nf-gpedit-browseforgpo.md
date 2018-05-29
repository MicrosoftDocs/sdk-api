---
UID: NF:gpedit.BrowseForGPO
title: BrowseForGPO function
author: windows-sdk-content
description: The BrowseForGPO function creates a GPO browser dialog box that allows the user to open or create a GPO.
old-location: policy\browseforgpo.htm
old-project: Policy
ms.assetid: ff144ae4-fc8c-499e-9086-75625b86693c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: BrowseForGPO, BrowseForGPO function [Group Policy], _win32_browseforgpo, gpedit/BrowseForGPO, policy.browseforgpo
ms.prod: windows
ms.technology: windows-sdk
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
-	BrowseForGPO
product: Windows
targetos: Windows
req.lib: Gpedit.lib
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# BrowseForGPO function


## -description


The
    <b>BrowseForGPO</b> function creates a GPO browser dialog box that allows the user to open or create a GPO.


## -parameters




### -param lpBrowseInfo [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/a0d038f2-66f1-4a79-b9e7-189cb57b80a9">GPOBROWSEINFO</a> structure that contains information used to initialize the dialog box. When 
the <b>BrowseForGPO</b> function returns, this structure contains information about the user's actions.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. If the user cancels or closes the dialog box, the return value is <b>HRESULT_FROM_WIN32</b>(<b>ERROR_CANCELLED</b>). Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/a0d038f2-66f1-4a79-b9e7-189cb57b80a9">GPOBROWSEINFO</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

