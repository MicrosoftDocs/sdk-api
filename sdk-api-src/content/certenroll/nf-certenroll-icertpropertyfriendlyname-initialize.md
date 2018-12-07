---
UID: NF:certenroll.ICertPropertyFriendlyName.Initialize
title: ICertPropertyFriendlyName::Initialize
author: windows-sdk-content
description: Initializes the object from the certificate display name.
old-location: security\icertpropertyfriendlyname_initialize_method.htm
tech.root: seccertenroll
ms.assetid: fb9a8108-f3d1-4a5c-bf3f-00002c085012
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertPropertyFriendlyName interface [Security],Initialize method, ICertPropertyFriendlyName.Initialize, ICertPropertyFriendlyName::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyFriendlyName interface, certenroll/ICertPropertyFriendlyName::Initialize, security.icertpropertyfriendlyname_initialize_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyFriendlyName.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyFriendlyName::Initialize


## -description


The <b>Initialize</b> method initializes the object from the certificate display name. This method is web enabled.


## -parameters




### -param strFriendlyName [in]

A <b>BSTR</b> variable that contains the name.  The string length cannot exceed 260 characters.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The string length exceeds 260 characters.

</td>
</tr>
</table>
 




## -remarks



Typically, you specify the display name in a user interface or from the command line before beginning the enrollment process so that the name can be associated with the dummy certificate in the request store. To retrieve that value and use it here, call the <a href="https://msdn.microsoft.com/en-us/library/Aa377866(v=VS.85).aspx">CertificateFriendlyName</a> on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375719(v=VS.85).aspx">FriendlyName</a> property to retrieve the display name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375646(v=VS.85).aspx">ICertPropertyDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375715(v=VS.85).aspx">ICertPropertyFriendlyName</a>
 

 

