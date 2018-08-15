---
UID: NF:msdrm.DRMGetUnboundLicenseAttributeCount
title: DRMGetUnboundLicenseAttributeCount function
author: windows-sdk-content
description: Retrieves the number of occurrences of an attribute within an object in an unbound license.
old-location: rm\drmgetunboundlicenseattributecount.htm
old-project: adrms_sdk
ms.assetid: ea462757-9df8-4b50-966b-5998e570f321
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMGetUnboundLicenseAttributeCount, DRMGetUnboundLicenseAttributeCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseAttributeCount, rm.drmgetunboundlicenseattributecount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetUnboundLicenseAttributeCount
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetUnboundLicenseAttributeCount function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseAttributeCount</b> function retrieves the number of occurrences of an attribute within an object in an unbound license.


## -parameters




### -param hQueryRoot [in]

A handle to a license or an object in the license, created using <a href="https://msdn.microsoft.com/d3e03d62-5202-4969-a4c7-5fbf89070436">DRMGetUnboundLicenseObject</a> or <a href="https://msdn.microsoft.com/2ae65ed2-7702-4e9b-b986-68b83ebe8bf5">DRMParseUnboundLicense</a>.


### -param wszAttributeType [in]

Name of the attribute to retrieve.


### -param pcAttributes [out]

Count of attribute occurrences one level down within the specified branch.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Certain attributes, such as maximum count, may appear more than once in a branch of a license. This method returns a count of these occurrences, so that an application can iterate through them or access a particular one. This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_SKUVALUE, the query will find nothing because the SKUVALUE appears at the second level or deeper (counting the license root as level 0).




## -see-also




<a href="https://msdn.microsoft.com/4ddf2920-95ea-47be-a5dd-b68eee2de29e">DRMGetUnboundLicenseAttribute</a>



<a href="https://msdn.microsoft.com/d3e03d62-5202-4969-a4c7-5fbf89070436">DRMGetUnboundLicenseObject</a>



<a href="https://msdn.microsoft.com/a1c2ae7e-a0be-482d-a366-70988cbc4616">DRMGetUnboundLicenseObjectCount</a>



<a href="https://msdn.microsoft.com/7496380a-2848-4353-a672-27fc5a9eed92">Querying Licenses</a>
 

 

