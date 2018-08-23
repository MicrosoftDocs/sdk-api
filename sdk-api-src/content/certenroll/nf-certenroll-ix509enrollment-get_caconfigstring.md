---
UID: NF:certenroll.IX509Enrollment.get_CAConfigString
title: IX509Enrollment::get_CAConfigString
author: windows-sdk-content
description: Retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.
old-location: security\ix509enrollment_caconfigstring_property.htm
old-project: seccertenroll
ms.assetid: 4a4478c8-a665-4ee1-9f3a-cad259e1c9ce
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CAConfigString property [Security], CAConfigString property [Security],IX509Enrollment interface, IX509Enrollment interface [Security],CAConfigString property, IX509Enrollment.CAConfigString, IX509Enrollment.get_CAConfigString, IX509Enrollment::CAConfigString, IX509Enrollment::get_CAConfigString, certenroll/IX509Enrollment::CAConfigString, certenroll/IX509Enrollment::get_CAConfigString, get_CAConfigString, security.ix509enrollment_caconfigstring_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IX509Enrollment.CAConfigString
 - IX509Enrollment.get_CAConfigString
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::get_CAConfigString


## -description


The <b>CAConfigString</b> property retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.

This property is read-only.


## -parameters


## -remarks



The configuration string contains the Domain Name System (DNS) name and the common name (CN) of the certification authority. The format of the string is "<i>CAComputerDNSName</i>\<i>CACommonName</i>".




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

