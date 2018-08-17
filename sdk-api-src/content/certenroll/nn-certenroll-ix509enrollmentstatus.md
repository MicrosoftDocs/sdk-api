---
UID: NN:certenroll.IX509EnrollmentStatus
title: IX509EnrollmentStatus
author: windows-sdk-content
description: The IX509EnrollmentStatus interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.
old-location: security\ix509enrollmentstatus.htm
old-project: seccertenroll
ms.assetid: fa5e3a10-7f00-46b6-b740-b72d78745bf7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509EnrollmentStatus, IX509EnrollmentStatus interface [Security], IX509EnrollmentStatus interface [Security],described, certenroll/IX509EnrollmentStatus, security.ix509enrollmentstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509EnrollmentStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509EnrollmentStatus interface


## -description


The <b>IX509EnrollmentStatus</b> interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509EnrollmentStatus</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509EnrollmentStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377820(v=VS.85).aspx">AppendText</a>
</td>
<td align="left" width="63%">
Appends a string to the status information contained in the <a href="https://msdn.microsoft.com/en-us/library/Aa377845(v=VS.85).aspx">Text</a> property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentStatus</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377826(v=VS.85).aspx">Display</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether to display the status information in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377832(v=VS.85).aspx">Error</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a value that identifies the error status of the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377829(v=VS.85).aspx">ErrorText</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the message associated with the error result code returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa377832(v=VS.85).aspx">Error</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether an item can be used during the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377844(v=VS.85).aspx">Status</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates the status of the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377845(v=VS.85).aspx">Text</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a message associated with the status of the enrollment process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

