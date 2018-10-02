---
UID: NE:wtsdefs.WTS_CERT_TYPE
title: WTS_CERT_TYPE
author: windows-sdk-content
description: Contains values that specify the type of certificate used to obtain a license.
old-location: termserv\wts_cert_type.htm
tech.root: TermServ
ms.assetid: bf3dcb94-e788-4c60-ad4e-001ca040c6b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WRDS_CERT_TYPE, WRDS_CERT_TYPE enumeration [Remote Desktop Services], WTS_CERT_TYPE, WTS_CERT_TYPE enumeration [Remote Desktop Services], WTS_CERT_TYPE_INVALID, WTS_CERT_TYPE_PROPRIETORY, WTS_CERT_TYPE_X509, termserv.wts_cert_type, wtsdefs/WRDS_CERT_TYPE, wtsdefs/WTS_CERT_TYPE, wtsdefs/WTS_CERT_TYPE_INVALID, wtsdefs/WTS_CERT_TYPE_PROPRIETORY, wtsdefs/WTS_CERT_TYPE_X509
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsdefs.h
api_name:
 - WTS_CERT_TYPE
product: Windows
targetos: Windows
req.typenames: WTS_CERT_TYPE
req.redist: 
---

# WTS_CERT_TYPE enumeration


## -description


Contains values that specify the type of certificate used to obtain a license.


## -enum-fields




### -field WTS_CERT_TYPE_INVALID

The certificate is not valid.


### -field WTS_CERT_TYPE_PROPRIETORY

The certificate is a custom type.


### -field WTS_CERT_TYPE_X509

The certificate adheres to the X.509 standard.


## -remarks



This enumeration is used by the <a href="https://msdn.microsoft.com/975a534e-03f1-4c8f-9de1-42144e31c8cb">WTS_LICENSE_CAPABILITIES</a> structure.



