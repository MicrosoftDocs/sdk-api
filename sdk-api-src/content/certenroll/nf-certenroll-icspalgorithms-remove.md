---
UID: NF:certenroll.ICspAlgorithms.Remove
title: ICspAlgorithms::Remove
author: windows-sdk-content
description: Removes an ICspAlgorithm object from the collection by index number.
old-location: security\icspalgorithms_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: 9116ca78-3b99-4b9a-97af-d01077e201f7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICspAlgorithms interface [Security],Remove method, ICspAlgorithms.Remove, ICspAlgorithms::Remove, Remove, Remove method [Security], Remove method [Security],ICspAlgorithms interface, certenroll/ICspAlgorithms::Remove, security.icspalgorithms_remove_method
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
 - ICspAlgorithms.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspAlgorithms::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">ICspAlgorithm</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375948(v=VS.85).aspx">ICspAlgorithms</a>
 

 

