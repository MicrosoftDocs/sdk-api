---
UID: NF:msdrm.DRMGetUnboundLicenseObject
title: DRMGetUnboundLicenseObject function
author: windows-sdk-content
description: Retrieves an object of a specified type in an unbound license.
old-location: rm\drmgetunboundlicenseobject.htm
tech.root: adrms_sdk
ms.assetid: d3e03d62-5202-4969-a4c7-5fbf89070436
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMGetUnboundLicenseObject, DRMGetUnboundLicenseObject function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseObject, rm.drmgetunboundlicenseobject
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
 - DRMGetUnboundLicenseObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetUnboundLicenseObject function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseObject</b> function retrieves an object of a specified type in an unbound license.


## -parameters




### -param hQueryRoot [in]

A handle to a license or object in the license, created using <b>DRMGetUnboundLicenseObject</b> or <a href="https://msdn.microsoft.com/2ae65ed2-7702-4e9b-b986-68b83ebe8bf5">DRMParseUnboundLicense</a>.


### -param wszSubObjectType [in]

Name of the object to find.


### -param iIndex [in]

Zero-based index indicating which instance to retrieve, if more than one exists.


### -param phSubQuery [out]

The retrieved object. Call <a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a> to close the  handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Each object can have several instances within a license. A license may contain many rights objects, for example. In this case, it may be necessary to iterate through all the objects in this class by first calling <a href="https://msdn.microsoft.com/a1c2ae7e-a0be-482d-a366-70988cbc4616">DRMGetUnboundLicenseObjectCount</a> to get a count of existing objects, and then looping through all instances, starting at zero and incrementing the <i>iWhich</i> value by one. If a specific object is sought, each retrieved object can be queried for its attributes, such as its name.

This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_OWNER, the query will find nothing because the OWNER object appears at the second level or deeper (counting the license root as level 0).

The <i>wszSubObjectType</i> parameter identifies an XrML node value as shown in the following example. Using g_wszQUERY_OBJECTTYPE in a query would return "Group Identity Licensor." The only object you can query for in an issuance license is g_wszQUERY_DISTRIBUTIONPOINT.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>&lt;PRINCIPAL internal-id="1"&gt;
  &lt;OBJECT type="Group Identity Licensor"&gt;
  &lt;ID type="Group Identity"&gt;someone@example.com&lt;/ID&gt;
  &lt;NAME&gt;Pavel's Group Identity&lt;/NAME&gt;
  &lt;/OBJECT&gt;</pre>
</td>
</tr>
</table></span></div>
Call <a href="https://msdn.microsoft.com/4902a6e2-e3b2-4f05-970c-aa4f80895762">DRMCloseQueryHandle</a>  to close the object handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/4ddf2920-95ea-47be-a5dd-b68eee2de29e">DRMGetUnboundLicenseAttribute</a>



<a href="https://msdn.microsoft.com/ea462757-9df8-4b50-966b-5998e570f321">DRMGetUnboundLicenseAttributeCount</a>



<a href="https://msdn.microsoft.com/a1c2ae7e-a0be-482d-a366-70988cbc4616">DRMGetUnboundLicenseObjectCount</a>



<a href="https://msdn.microsoft.com/7496380a-2848-4353-a672-27fc5a9eed92">Querying Licenses</a>
 

 

