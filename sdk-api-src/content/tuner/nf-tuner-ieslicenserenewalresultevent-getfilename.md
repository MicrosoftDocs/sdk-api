---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetFileName
title: IESLicenseRenewalResultEvent::GetFileName (tuner.h)
author: windows-sdk-content
description: Gets the file name for the license to renew from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent_getfilename.htm
tech.root: mstv
ms.assetid: 6ef49a38-c005-4731-a1cb-d5a63ea94e71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [DirectShow], GetFileName method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetFileName method, IESLicenseRenewalResultEvent.GetFileName, IESLicenseRenewalResultEvent::GetFileName, mstv.ieslicenserenewalresultevent_getfilename, tuner/IESLicenseRenewalResultEvent::GetFileName
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESLicenseRenewalResultEvent.GetFileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESLicenseRenewalResultEvent::GetFileName


## -description


Gets the file name for the license to renew  from a <b>LicenseRenewalResult</b> event.


## -parameters




### -param pbstrFilename [out, retval]

Pointer to a buffer that receives the file name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>
 

 

