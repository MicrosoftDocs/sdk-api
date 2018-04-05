---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetFileName
title: IESLicenseRenewalResultEvent::GetFileName method
author: windows-driver-content
description: Gets the file name for the license to renew from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent_getfilename.htm
old-project: mstv
ms.assetid: 6ef49a38-c005-4731-a1cb-d5a63ea94e71
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetFileName method [DirectShow], GetFileName method [DirectShow], IESLicenseRenewalResultEvent interface, GetFileName,IESLicenseRenewalResultEvent.GetFileName, IESLicenseRenewalResultEvent, IESLicenseRenewalResultEvent interface [DirectShow], GetFileName method, IESLicenseRenewalResultEvent::GetFileName, mstv.ieslicenserenewalresultevent_getfilename, tuner/IESLicenseRenewalResultEvent::GetFileName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESLicenseRenewalResultEvent.GetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetFileName method


## -description


Gets the file name for the license to renew  from a <b>LicenseRenewalResult</b> event.


## -parameters




### -param pbstrFilename [out, retval]

Pointer to a buffer that receives the file name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 

