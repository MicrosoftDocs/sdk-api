---
UID: NF:certenroll.IObjectIds.Add
title: IObjectIds::Add (certenroll.h)
author: windows-sdk-content
description: Adds an IObjectId object to the collection.
old-location: security\iobjectids_add_method.htm
tech.root: seccertenroll
ms.assetid: 93f27993-2dba-4aec-9b63-cfd4dd56bbda
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IObjectIds interface, IObjectIds interface [Security],Add method, IObjectIds.Add, IObjectIds::Add, certenroll/IObjectIds::Add, security.iobjectids_add_method
ms.topic: method
f1_keywords: 
 - "certenroll/IObjectIds.Add"
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
 - IObjectIds.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectIds::Add


## -description


The <b>Add</b> method adds an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the object identifier to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a>
 

 

