---
UID: NF:certenroll.IObjectIds.Remove
title: IObjectIds::Remove (certenroll.h)
author: windows-sdk-content
description: Removes an IObjectId object from the collection by index value.
old-location: security\iobjectids_remove_method.htm
tech.root: seccertenroll
ms.assetid: c8b9508d-f64a-453f-a336-0da47b2ccdec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjectIds interface [Security],Remove method, IObjectIds.Remove, IObjectIds::Remove, Remove, Remove method [Security], Remove method [Security],IObjectIds interface, certenroll/IObjectIds::Remove, security.iobjectids_remove_method
ms.topic: method
f1_keywords: 
 - "certenroll/IObjectIds.Remove"
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
 - IObjectIds.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectIds::Remove


## -description


The <b>Remove</b> method removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
 

 

