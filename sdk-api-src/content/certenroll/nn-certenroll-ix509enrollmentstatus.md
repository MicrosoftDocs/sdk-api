---
UID: NN:certenroll.IX509EnrollmentStatus
title: IX509EnrollmentStatus
author: windows-sdk-content
description: The IX509EnrollmentStatus interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.
old-location: security\ix509enrollmentstatus.htm
tech.root: SecCertEnroll
ms.assetid: fa5e3a10-7f00-46b6-b740-b72d78745bf7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509EnrollmentStatus, IX509EnrollmentStatus interface [Security], IX509EnrollmentStatus interface [Security],described, certenroll/IX509EnrollmentStatus, security.ix509enrollmentstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IX509EnrollmentStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EnrollmentStatus interface


## -description


The <b>IX509EnrollmentStatus</b> interface can be used to specify or retrieve detailed error information about a certificate enrollment transaction.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EnrollmentStatus</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509EnrollmentStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/aa7c3325-c897-49e3-b38c-ff1efead5f26">AppendText</a>
</td>
<td align="left" width="63%">
Appends a string to the status information contained in the <a href="https://msdn.microsoft.com/071c4040-cdcf-4a01-918d-397726a235ed">Text</a> property.

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

<a href="https://msdn.microsoft.com/91ac74af-8e59-42fc-bca8-d7ef96a1fed0">Display</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether to display the status information in a user interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/397ed934-5ec8-4653-ada4-e966f68cbbf2">Error</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a value that identifies the error status of the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3dc46598-5fd6-4462-be93-2358605d6783">ErrorText</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the message associated with the error result code returned by the <a href="https://msdn.microsoft.com/397ed934-5ec8-4653-ada4-e966f68cbbf2">Error</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9050f394-ccad-4a6e-90bc-53af3a874f91">Selected</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates whether an item can be used during the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ca1105eb-a29a-458d-abbb-34c9b67d7c8a">Status</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value that indicates the status of the enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/071c4040-cdcf-4a01-918d-397726a235ed">Text</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a message associated with the status of the enrollment process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

