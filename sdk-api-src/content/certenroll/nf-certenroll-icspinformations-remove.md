---
UID: NF:certenroll.ICspInformations.Remove
title: ICspInformations::Remove (certenroll.h)
author: windows-sdk-content
description: Removes an ICspInformation object from the collection by index number.
old-location: security\icspinformations_remove_method.htm
tech.root: seccertenroll
ms.assetid: cbf427d8-3f66-4a54-a226-2060c58924b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICspInformations interface [Security],Remove method, ICspInformations.Remove, ICspInformations::Remove, Remove, Remove method [Security], Remove method [Security],ICspInformations interface, certenroll/ICspInformations::Remove, security.icspinformations_remove_method
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
 - ICspInformations.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformations::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>
 

 

