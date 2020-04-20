---
UID: NF:certenroll.IX509Enrollment.get_CAConfigString
title: IX509Enrollment::get_CAConfigString (certenroll.h)
description: Retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.helpviewer_keywords: ["CAConfigString property [Security]","CAConfigString property [Security]","IX509Enrollment interface","IX509Enrollment interface [Security]","CAConfigString property","IX509Enrollment.CAConfigString","IX509Enrollment.get_CAConfigString","IX509Enrollment::CAConfigString","IX509Enrollment::get_CAConfigString","certenroll/IX509Enrollment::CAConfigString","certenroll/IX509Enrollment::get_CAConfigString","get_CAConfigString","security.ix509enrollment_caconfigstring_property"]
old-location: security\ix509enrollment_caconfigstring_property.htm
tech.root: seccertenroll
ms.assetid: 4a4478c8-a665-4ee1-9f3a-cad259e1c9ce
ms.date: 12/05/2018
ms.keywords: CAConfigString property [Security], CAConfigString property [Security],IX509Enrollment interface, IX509Enrollment interface [Security],CAConfigString property, IX509Enrollment.CAConfigString, IX509Enrollment.get_CAConfigString, IX509Enrollment::CAConfigString, IX509Enrollment::get_CAConfigString, certenroll/IX509Enrollment::CAConfigString, certenroll/IX509Enrollment::get_CAConfigString, get_CAConfigString, security.ix509enrollment_caconfigstring_property
f1_keywords:
- certenroll/IX509Enrollment.CAConfigString
dev_langs:
- c++
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
- IX509Enrollment.CAConfigString
- IX509Enrollment.get_CAConfigString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509Enrollment::get_CAConfigString


## -description


The <b>CAConfigString</b> property retrieves the configuration string that identifies the certification authority (CA) to which the certificate request was submitted.

This property is read-only.


## -parameters


## -remarks



The configuration string contains the Domain Name System (DNS) name and the common name (CN) of the certification authority. The format of the string is "<i>CAComputerDNSName</i>\<i>CACommonName</i>".




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>
 

 

