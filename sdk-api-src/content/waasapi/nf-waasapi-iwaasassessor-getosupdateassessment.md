---
UID: NF:waasapi.IWaaSAssessor.GetOSUpdateAssessment
title: IWaaSAssessor::GetOSUpdateAssessment (waasapi.h)
description: Gets the OS update assessment by comparing the latest release OS version from Microsoft to the OS build running on the device.
helpviewer_keywords: ["GetOSUpdateAssessment","GetOSUpdateAssessment method","GetOSUpdateAssessment method","IWaaSAssessor interface","IWaaSAssessor interface","GetOSUpdateAssessment method","IWaaSAssessor.GetOSUpdateAssessment","IWaaSAssessor::GetOSUpdateAssessment","base.iwaasassessor_getosupdateassessment","waasapi/IWaaSAssessor::GetOSUpdateAssessment"]
old-location: base\iwaasassessor_getosupdateassessment.htm
tech.root: winprog
ms.assetid: 3123362E-6A1C-49BD-BE9C-0B8506EA944B
ms.date: 12/05/2018
ms.keywords: GetOSUpdateAssessment, GetOSUpdateAssessment method, GetOSUpdateAssessment method,IWaaSAssessor interface, IWaaSAssessor interface,GetOSUpdateAssessment method, IWaaSAssessor.GetOSUpdateAssessment, IWaaSAssessor::GetOSUpdateAssessment, base.iwaasassessor_getosupdateassessment, waasapi/IWaaSAssessor::GetOSUpdateAssessment
req.header: waasapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WaaSAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWaaSAssessor::GetOSUpdateAssessment
 - waasapi/IWaaSAssessor::GetOSUpdateAssessment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - waasapi.h
api_name:
 - IWaaSAssessor.GetOSUpdateAssessment
---

# IWaaSAssessor::GetOSUpdateAssessment


## -description

Gets the OS update assessment by comparing the latest release OS version from Microsoft to the OS build running on the device.

## -parameters

### -param result [out, retval]

On success, contains a pointer to the OS update assessment.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

<b>GetOSUpdateAssessment</b> retrieves the OS update assessment. The assessment provides information on updates applicable to a device: specifically, if the OS on the device is up-to-date. If the OS is not up-to-date, the assessment provides some reasons why. The assessment also suggests the potential impact being out-of-date has on the device.

Your code must have administrator privileges to use the <b>GetOSUpdateAssessment</b> method. For more details about developing applications that require administrator privileges, see [this article](/windows/win32/secauthz/developing-applications-that-require-administrator-privilege).

## -see-also

<a href="/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor">IWaaSAssessor</a>