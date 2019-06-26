---
UID: NF:msdrm.DRMGetBoundLicenseObjectCount
title: DRMGetBoundLicenseObjectCount function (msdrm.h)
author: windows-sdk-content
description: Retrieves the number of occurrences of an object within a specified branch of a license.
old-location: rm\drmgetboundlicenseobjectcount.htm
tech.root: AdRms_Sdk
ms.assetid: 1bb9a9b7-f254-4c2b-a7b0-5e9b99c92488
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMGetBoundLicenseObjectCount, DRMGetBoundLicenseObjectCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetBoundLicenseObjectCount, rm.drmgetboundlicenseobjectcount
ms.topic: function
f1_keywords: 
 - "msdrm/DRMGetBoundLicenseObjectCount"
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetBoundLicenseObjectCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRMGetBoundLicenseObjectCount function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetBoundLicenseObjectCount</b> function retrieves the number of occurrences of an object within a specified branch of a license.


## -parameters




### -param hQueryRoot [in]

A handle to the branch of the license to query, from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobject">DRMGetBoundLicenseObject</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.


### -param wszSubObjectType [in]

The type of XrML object to find. For more information, see Remarks.


### -param pcSubObjects [out]

Number of objects of this type within this branch.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



Certain license structures, such as a <b>RIGHT</b> structure, may have multiple instances in a license. This method returns a count of these occurrences, so that an application can iterate through them to access a particular one by using <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobject">DRMGetBoundLicenseObject</a>.

The Active Directory Rights Management system exposes an object-oriented interface to the underlying license XrML. This function, along with other <b>DRMGetBoundLicense_xxx</b> functions, allows an application to navigate this structure. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattribute">DRMGetBoundLicenseAttribute</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattributecount">DRMGetBoundLicenseAttributeCount</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobject">DRMGetBoundLicenseObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>
 

 

