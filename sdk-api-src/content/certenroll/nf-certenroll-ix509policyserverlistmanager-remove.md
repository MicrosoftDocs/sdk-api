---
UID: NF:certenroll.IX509PolicyServerListManager.Remove
title: IX509PolicyServerListManager::Remove method
author: windows-driver-content
description: Removes an IX509PolicyServerUrl object from the collection by index number.
old-location: security\ix509policyserverlistmanager_remove.htm
old-project: SecCertEnroll
ms.assetid: c2e59087-a62b-4013-9a16-fedd03b2c286
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509PolicyServerListManager, IX509PolicyServerListManager interface [Security], Remove method, IX509PolicyServerListManager::Remove, Remove method [Security], Remove method [Security], IX509PolicyServerListManager interface, Remove,IX509PolicyServerListManager.Remove, certenroll/IX509PolicyServerListManager::Remove, security.ix509policyserverlistmanager_remove
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509PolicyServerListManager.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PolicyServerListManager::Remove method


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/ad9d61ec-f607-4f71-ad8a-28d821e29c27">IX509PolicyServerUrl</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/a9fe4f4b-a35d-40e6-b99a-a89f58e79250">IX509PolicyServerListManager</a>
 

 

