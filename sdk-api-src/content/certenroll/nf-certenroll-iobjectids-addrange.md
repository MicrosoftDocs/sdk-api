---
UID: NF:certenroll.IObjectIds.AddRange
title: IObjectIds::AddRange (certenroll.h)
author: windows-sdk-content
description: Adds a range of IObjectId objects to the collection.
old-location: security\iobjectids_addrange_method.htm
tech.root: seccertenroll
ms.assetid: bf7a85a3-201b-413e-a1da-1e54b55771cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],IObjectIds interface, IObjectIds interface [Security],AddRange method, IObjectIds.AddRange, IObjectIds::AddRange, certenroll/IObjectIds::AddRange, security.iobjectids_addrange_method
ms.topic: method
f1_keywords: 
 - "certenroll/IObjectIds.AddRange"
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
 - IObjectIds.AddRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectIds::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> objects to the collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> interface that represents the collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
 

 

