---
UID: NF:msdrm.DRMGetBoundLicenseObject
title: DRMGetBoundLicenseObject function (msdrm.h)
author: windows-sdk-content
description: Returns an object from a bound license.
old-location: rm\drmgetboundlicenseobject.htm
tech.root: AdRms_Sdk
ms.assetid: d1be0668-fb5a-4541-92dc-34255ba3fdad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMGetBoundLicenseObject, DRMGetBoundLicenseObject function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetBoundLicenseObject, rm.drmgetboundlicenseobject
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
 - DRMGetBoundLicenseObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetBoundLicenseObject function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetBoundLicenseObject</b> function returns an object from a bound license.


## -parameters




### -param hQueryRoot [in]

A handle to a license or license object, from a previous call to this function or from <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.


### -param wszSubObjectType [in]

The type of XrML object to find. For more information, see Remarks.


### -param iWhich [in]

Zero-based index specifying which occurrence to retrieve.


### -param phSubObject [out]

A handle to the returned license object. Call <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



There are many kinds of objects in a license, such as principals, rights, and access conditions. The Active Directory Rights Management system exposes an object-oriented interface to the underlying license XrML. This function, along with other <b>DRMGetBoundLicense_xxx</b> functions, allows an application to navigate this structure. For more information, see <a href="https://msdn.microsoft.com/7496380a-2848-4353-a672-27fc5a9eed92">Querying Licenses</a>. On first call, use the license handle itself as the query root.

On first call, this function takes the <b>DRMHANDLE</b> returned by <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.

The <i>wszSubObjectType</i> parameter identifies an XrML type as shown in the following example. Using g_wszQUERY_OBJECTTYPE to query the XrML would return "Group Identity Licensor."


```cpp
<PRINCIPAL internal-id="1">
  <OBJECT type="Group Identity Licensor">
  <ID type="Group Identity">someone@example.com</ID> 
  <NAME>Pavel's Group Identity</NAME> 
  </OBJECT>
```


Call <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> to close the handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/715fb3e6-6b1e-4136-9c25-efcde2015d6f">DRMGetBoundLicenseAttribute</a>



<a href="https://msdn.microsoft.com/5b3814f5-bab7-4b46-a38b-54406cb8cae0">DRMGetBoundLicenseAttributeCount</a>



<a href="https://msdn.microsoft.com/1bb9a9b7-f254-4c2b-a7b0-5e9b99c92488">DRMGetBoundLicenseObjectCount</a>



<a href="https://msdn.microsoft.com/7496380a-2848-4353-a672-27fc5a9eed92">Querying Licenses</a>
 

 

