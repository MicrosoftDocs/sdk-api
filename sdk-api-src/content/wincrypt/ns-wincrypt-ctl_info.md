---
UID: NS:wincrypt._CTL_INFO
title: CTL_INFO (wincrypt.h)
author: windows-sdk-content
description: Contains the information stored in a Certificate Trust List (CTL).
old-location: security\ctl_info.htm
tech.root: SecCrypto
ms.assetid: 83b015b5-a650-4a81-a9f0-c3e8a9805c81
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCTL_INFO, CTL_INFO, CTL_INFO structure [Security], CTL_V1, PCTL_INFO, PCTL_INFO structure pointer [Security], _crypto2_ctl_info, security.ctl_info, wincrypt/CTL_INFO, wincrypt/PCTL_INFO"
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_INFO
product: Windows
targetos: Windows
req.typenames: CTL_INFO, *PCTL_INFO
req.redist: 
ms.custom: 19H1
---

# CTL_INFO structure


## -description


The <b>CTL_INFO</b> structure contains the information stored in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Trust List</a> (CTL).


## -struct-fields




### -field dwVersion

The CTL's version number. Currently defined version numbers are shown in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTL_V1"></a><a id="ctl_v1"></a><dl>
<dt><b>CTL_V1</b></dt>
</dl>
</td>
<td width="60%">
Version 1

</td>
</tr>
</table>
 


### -field SubjectUsage


<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a> structure identifying the intended usage of the list as a sequence of object identifiers. This is the same as in the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">Enhanced Key Usage</a> extension.


### -field ListIdentifier

A
						<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that includes a byte string that uniquely identifies the list. This member is used to augment the <b>SubjectUsage</b> and further specifies the list when desired.


### -field SequenceNumber

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains a monotonically increasing number for each update of the CTL.


### -field ThisUpdate

Indication of the date and time of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) published. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte year precise to milliseconds with a 4-byte year.


### -field NextUpdate

Indication of the date and time for the CRL's next available scheduled update. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte date time precise to milliseconds with a 4-byte year.


### -field SubjectAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the algorithm type of the <b>SubjectIdentifier</b> in <a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a> members of the <b>rgCTLEntry</b> member array. The structure also includes additional parameters used by the algorithm.


### -field cCTLEntry

Number of elements in the <b>rgCTLEntry</b> member array.


### -field rgCTLEntry

Array of 
<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a> structures.


### -field cExtension

Number of elements in the <b>rgExtension</b> array.


### -field rgExtension

Array of 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/ebc63847-b641-4205-b15c-7b32c1426c21">CTL_ENTRY</a>



<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a>
 

 

