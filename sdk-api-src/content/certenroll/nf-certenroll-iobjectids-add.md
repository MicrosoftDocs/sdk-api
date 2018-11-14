---
UID: NF:certenroll.IObjectIds.Add
title: IObjectIds::Add
author: windows-sdk-content
description: Adds an IObjectId object to the collection.
old-location: security\iobjectids_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 93f27993-2dba-4aec-9b63-cfd4dd56bbda
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Add, Add method [Security], Add method [Security],IObjectIds interface, IObjectIds interface [Security],Add method, IObjectIds.Add, IObjectIds::Add, certenroll/IObjectIds::Add, security.iobjectids_add_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
- apiref
: 
- COM
: 
- certenroll.h
: 
- IObjectIds.Add
: 
---

# IObjectIds::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that represents the object identifier to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a>
 

 

