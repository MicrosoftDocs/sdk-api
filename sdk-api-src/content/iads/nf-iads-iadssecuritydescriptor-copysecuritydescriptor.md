---
UID: NF:iads.IADsSecurityDescriptor.CopySecurityDescriptor
title: IADsSecurityDescriptor::CopySecurityDescriptor
author: windows-sdk-content
description: The IADsSecurityDescriptor::CopySecurityDescriptor method copies an ADSI security descriptor object that holds security data about an object.
old-location: adsi\iadssecuritydescriptor_copysecuritydescriptor.htm
old-project: ADSI
ms.assetid: fe30a23a-ccf0-4852-bfcc-9f5a010bd0ec
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CopySecurityDescriptor, CopySecurityDescriptor method [ADSI], CopySecurityDescriptor method [ADSI],IADsSecurityDescriptor interface, IADsSecurityDescriptor interface [ADSI],CopySecurityDescriptor method, IADsSecurityDescriptor.CopySecurityDescriptor, IADsSecurityDescriptor::CopySecurityDescriptor, _ds_iadssecuritydescriptor_copysecuritydescriptor, adsi.iadssecuritydescriptor__copysecuritydescriptor, adsi.iadssecuritydescriptor_copysecuritydescriptor, iads/IADsSecurityDescriptor::CopySecurityDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsSecurityDescriptor.CopySecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsSecurityDescriptor::CopySecurityDescriptor


## -description


The <b>IADsSecurityDescriptor::CopySecurityDescriptor</b> method copies an ADSI security descriptor object that holds security data about an object.


## -parameters




### -param ppSecurityDescriptor [out]

Pointer to a pointer to a security descriptor object.


## -returns



This method returns the standard return values, including <b>E_INVALIDARG</b>, <b>E_OUTOFMEMORY</b>, <b>E_UNEXPECTED</b>, and <b>E_FAIL</b>, as well as <b>S_OK</b>. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>
 

 

