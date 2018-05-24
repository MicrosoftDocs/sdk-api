---
UID: NF:msdrm.DRMSetApplicationSpecificData
title: DRMSetApplicationSpecificData function
author: windows-driver-content
description: Allows an issuance license to store arbitrary name-value pairs for use by the content-consuming application.
old-location: rm\drmsetapplicationspecificdata.htm
old-project: AdRms_Sdk
ms.assetid: 659b2d73-1160-4e5a-8779-4bb272653c54
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMSetApplicationSpecificData, DRMSetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetApplicationSpecificData, rm.drmsetapplicationspecificdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMSetApplicationSpecificData
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetApplicationSpecificData function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetApplicationSpecificData</b> function allows an issuance license to store arbitrary name-value pairs for use by the content-consuming application.


## -parameters




### -param hIssuanceLicense [in]

A handle to an issuance license.


### -param fDelete [in]

A flag that indicates whether to add or delete this name-value pair.   <b>FALSE</b> indicates add; <b>TRUE</b> indicates delete.


### -param wszName [in]

The name of the data.


### -param wszValue [in]

The value of the data.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The values stored can be used to pass information to a consuming application, such as the version and name of the publishing application, contact information, or any other arbitrary information. Information is stored in a zero-based array and is retrieved by using the <a href="https://msdn.microsoft.com/49b23f00-bc73-4f51-8bbe-f523ae2408d7">DRMGetApplicationSpecificData</a> function. This function is used both to store a value or delete a stored value, depending on the flag passed in.

One data pair that is processed by an Active Directory Rights Management Services (AD RMS) server is the string pair "Allow_Server_Editing"/"True". When an issuance license has this value pair, it will allow the service, or any trusted service, to reuse the content key. This allows an issuance license to be republished by using the AD RMS SOAP function <a href="https://msdn.microsoft.com/ad22a0bc-8b75-4534-a94a-4520e2397371">EditIssuanceLicense</a>. This function takes in an old issuance license (with this name-value pair) and a new unsigned issuance license, and puts the content key into the new license. The pair "Allow_Server_Editing"/"True" must be added to the new issuance license if you want to allow publishing again.

To prevent republishing, remove this name-value pair or do not include it (do not add the data item with the value "False").




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/49b23f00-bc73-4f51-8bbe-f523ae2408d7">DRMGetApplicationSpecificData</a>
 

 

