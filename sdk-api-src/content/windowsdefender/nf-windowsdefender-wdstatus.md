---
UID: NF:windowsdefender.WDStatus
title: WDStatus function
author: windows-sdk-content
description: Returns the current status of Windows Defender.
old-location: lwef\defender_wdstatus.htm
old-project: lwef
ms.assetid: 885729a7-13a4-401e-ad7b-4f679777531b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WDStatus, WDStatus function [Legacy Windows Environment Features], lwef.defender_wdstatus, shell.defender_wdstatus, shell_defender_WDStatus, windowsdefender/WDStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: windowsdefender.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MpClient.dll
api_name:
 - WDStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: MpClient.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WDStatus function


## -description


Returns the current status of Windows Defender. 


## -parameters




### -param pfEnabled [out]

Type: <b>BOOL*</b>

The status of Windows Defender as a boolean. <b>TRUE</b> means Windows Defender is in enabled status. <b>FALSE</b> means Windows Defender is in disabled status. 


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a12d3b2a-6873-4ef4-90d6-08dbd5feb959">WDEnable</a>
 

 

