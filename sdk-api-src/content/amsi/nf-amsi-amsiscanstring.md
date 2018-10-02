---
UID: NF:amsi.AmsiScanString
title: AmsiScanString function
author: windows-sdk-content
description: Scans a string for malware.
old-location: amsi\amsiscanstring.htm
tech.root: AMSI
ms.assetid: 7D26C57B-014B-4506-A29D-33699808B111
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AmsiScanString, AmsiScanString function [Antimalware Scan Interface], amsi.amsiscanstring, amsi/AmsiScanString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiScanString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AmsiScanString function


## -description


Scans a string for malware.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


### -param string [in]

The string to be scanned.


### -param contentName [in]

The filename, URL, unique script ID, or similar of the content being scanned.


### -param amsiSession [in, optional]

If multiple scan requests are to be correlated within a session, set <i>session</i> to the handle of type HAMSISESSION that was initially received from <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>. Otherwise, set <i>session</i> to <b>nullptr</b>.


### -param result [out]

The result of the scan. See <a href="https://msdn.microsoft.com/3D7C74E3-BB09-4C53-930D-72D352374151">AMSI_RESULT</a>.

An app should use <a href="https://msdn.microsoft.com/1C7B48D9-FD1C-48B5-AA7F-0ED7382E106A">AmsiResultIsMalware</a> to determine whether the content should be blocked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3D7C74E3-BB09-4C53-930D-72D352374151">AMSI_RESULT</a>



<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>



<a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>



<a href="https://msdn.microsoft.com/1C7B48D9-FD1C-48B5-AA7F-0ED7382E106A">AmsiResultIsMalware</a>
 

 

