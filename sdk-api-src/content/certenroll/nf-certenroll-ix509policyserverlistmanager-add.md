---
UID: NF:certenroll.IX509PolicyServerListManager.Add
title: IX509PolicyServerListManager::Add method
author: windows-driver-content
description: Adds an IX509PolicyServerUrl object to the collection.
old-location: security\ix509policyserverlistmanager_add.htm
old-project: SecCertEnroll
ms.assetid: f1f22d27-96bf-47f7-8572-5f3842797c18
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: Add method [Security], Add method [Security], IX509PolicyServerListManager interface, Add,IX509PolicyServerListManager.Add, IX509PolicyServerListManager, IX509PolicyServerListManager interface [Security], Add method, IX509PolicyServerListManager::Add, certenroll/IX509PolicyServerListManager::Add, security.ix509policyserverlistmanager_add
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
-	IX509PolicyServerListManager.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PolicyServerListManager::Add method


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/ad9d61ec-f607-4f71-ad8a-28d821e29c27">IX509PolicyServerUrl</a> object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://msdn.microsoft.com/ad9d61ec-f607-4f71-ad8a-28d821e29c27">IX509PolicyServerUrl</a> object to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/a9fe4f4b-a35d-40e6-b99a-a89f58e79250">IX509PolicyServerListManager</a>
 

 

