---
UID: NS:iketypes.IKEEXT_CERT_NAME0_
title: IKEEXT_CERT_NAME0 (iketypes.h)
author: windows-sdk-content
description: Specifies certificate selection &#0034;subject&#0034; criteria for an authentication method.
old-location: fwp\ikeext_cert_name0.htm
tech.root: fwp
ms.assetid: 50e04e10-cae1-4fcd-990e-3e9b538627ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_NAME0, IKEEXT_CERT_NAME0 structure [Filtering], fwp.ikeext_cert_name0, iketypes/IKEEXT_CERT_NAME0
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - iketypes.h
api_name:
 - IKEEXT_CERT_NAME0
product: Windows
targetos: Windows
req.typenames: IKEEXT_CERT_NAME0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_CERT_NAME0 structure


## -description


The <b>IKEEXT_CERT_NAME0</b> structure specifies certificate selection "subject" criteria for an authentication method.


## -struct-fields




### -field nameType

Type: <b><a href="https://msdn.microsoft.com/ec59d6b2-3bfc-4e5b-9222-609d3141db5c">IKEEXT_CERT_CRITERIA_NAME_TYPE</a></b>

The type of NAME field.


### -field certName

Type: <b>LPWSTR</b>

The string to be used for matching the "subject" criteria.


## -see-also




<a href="https://msdn.microsoft.com/ec59d6b2-3bfc-4e5b-9222-609d3141db5c">IKEEXT_CERT_CRITERIA_NAME_TYPE</a>
 

 

