---
UID: NF:certenroll.ICspStatus.get_EnrollmentStatus
title: ICspStatus::get_EnrollmentStatus
author: windows-sdk-content
description: Retrieves an IX509EnrollmentStatus object that contains information about the certificate enrollment.
old-location: security\icspstatus_enrollmentstatus_property.htm
old-project: seccertenroll
ms.assetid: 56798477-ec12-47b6-a226-d20258677033
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnrollmentStatus property [Security], EnrollmentStatus property [Security],ICspStatus interface, ICspStatus interface [Security],EnrollmentStatus property, ICspStatus.EnrollmentStatus, ICspStatus.get_EnrollmentStatus, ICspStatus::EnrollmentStatus, ICspStatus::get_EnrollmentStatus, certenroll/ICspStatus::EnrollmentStatus, certenroll/ICspStatus::get_EnrollmentStatus, get_EnrollmentStatus, security.icspstatus_enrollmentstatus_property
ms.prod: windows
ms.technology: windows-sdk
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
 - ICspStatus.EnrollmentStatus
 - ICspStatus.get_EnrollmentStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspStatus::get_EnrollmentStatus


## -description


The <b>EnrollmentStatus</b> property retrieves an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object that contains information about the certificate enrollment.

This property is read-only.


## -parameters


## -remarks



This property returns an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object. This object is typically populated when you create a PKCS #10 certificate request. The following three properties returned by this object provide information about the  provider/algorithm pair represented by an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object:<ul>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/dn915285">Display</a> property specifies whether the provider and algorithm should be displayed in a user interface.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property specifies whether the provider and algorithm can be used to create a key pair for a certificate request.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property specifies whether the provider and algorithm were skipped or resulted in an error during request initialization.</li>
</ul>


To understand how these properties are important, assume that a certificate request is based on a template that specifies a particular provider and algorithm. The <a href="https://msdn.microsoft.com/library/windows/hardware/dn915285">Display</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> properties for this provider/algorithm pair are enabled. For other <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects, one or both of these properties may not be enabled. For more complete examples, see the <a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a> property.

The <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property is set to <b>EnrollUnknown</b> when the <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object is first created. If a provider/algorithm pair is not selected, the status may be set to <b>EnrollSkipped</b>. The status will be set to <b>EnrollError</b> if key creation fails for the selected provider and algorithm during certificate initialization.




## -see-also




<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>



<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
 

 

