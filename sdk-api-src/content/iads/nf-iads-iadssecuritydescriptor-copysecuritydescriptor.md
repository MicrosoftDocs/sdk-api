---
UID: NF:iads.IADsSecurityDescriptor.CopySecurityDescriptor
title: IADsSecurityDescriptor::CopySecurityDescriptor (iads.h)
author: windows-sdk-content
description: The IADsSecurityDescriptor::CopySecurityDescriptor method copies an ADSI security descriptor object that holds security data about an object.
old-location: adsi\iadssecuritydescriptor_copysecuritydescriptor.htm
tech.root: adsi
ms.assetid: fe30a23a-ccf0-4852-bfcc-9f5a010bd0ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CopySecurityDescriptor, CopySecurityDescriptor method [ADSI], CopySecurityDescriptor method [ADSI],IADsSecurityDescriptor interface, IADsSecurityDescriptor interface [ADSI],CopySecurityDescriptor method, IADsSecurityDescriptor.CopySecurityDescriptor, IADsSecurityDescriptor::CopySecurityDescriptor, _ds_iadssecuritydescriptor_copysecuritydescriptor, adsi.iadssecuritydescriptor__copysecuritydescriptor, adsi.iadssecuritydescriptor_copysecuritydescriptor, iads/IADsSecurityDescriptor::CopySecurityDescriptor
ms.topic: method
f1_keywords: ["iads/IADsSecurityDescriptor.CopySecurityDescriptor"]
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityDescriptor.CopySecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsSecurityDescriptor::CopySecurityDescriptor


## -description


The <b>IADsSecurityDescriptor::CopySecurityDescriptor</b> method copies an ADSI security descriptor object that holds security data about an object.


## -parameters




### -param ppSecurityDescriptor [out]

Pointer to a pointer to a security descriptor object.


## -returns



This method returns the standard return values, including <b>E_INVALIDARG</b>, <b>E_OUTOFMEMORY</b>, <b>E_UNEXPECTED</b>, and <b>E_FAIL</b>, as well as <b>S_OK</b>. For more information about other return values, see  <a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>
 

 

