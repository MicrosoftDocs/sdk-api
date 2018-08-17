---
UID: NF:certenroll.IObjectIds.AddRange
title: IObjectIds::AddRange
author: windows-sdk-content
description: Adds a range of IObjectId objects to the collection.
old-location: security\iobjectids_addrange_method.htm
old-project: seccertenroll
ms.assetid: bf7a85a3-201b-413e-a1da-1e54b55771cc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],IObjectIds interface, IObjectIds interface [Security],AddRange method, IObjectIds.AddRange, IObjectIds::AddRange, certenroll/IObjectIds::AddRange, security.iobjectids_addrange_method
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
 - IObjectIds.AddRange
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectIds::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> objects to the collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a> interface that represents the collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376785(v=VS.85).aspx">IObjectIds</a>
 

 

