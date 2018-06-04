---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAttachmentExecute::SetLocalPath


## -description


Sets and stores the path to the file.


## -parameters




### -param pszLocalPath [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the local path where the attachment file is to be stored.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling <b>IAttachmentExecute::SetLocalPath</b> is required.

When the attachment is approved for execution by the user (either through policy or prompt), the path specified by this method is used. If only <a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a> was called before calling <a href="https://msdn.microsoft.com/ff6a0aa8-4d14-4074-b084-be117b01c77a">IAttachmentExecute::CheckPolicy</a> and <a href="https://msdn.microsoft.com/01c01abf-df7a-411b-979b-ddd8da569f91">IAttachmentExecute::Prompt</a>, that trust could be revoked if the assumed local path was different from that set by <b>IAttachmentExecute::SetLocalPath</b>. Trust can be granted by various Zone APIs, antivirus services, file type information, policies as well as other system trust providers.

<b>IAttachmentExecute::SetLocalPath</b> must be called before calling <a href="https://msdn.microsoft.com/80cbbb6c-c6f1-4937-9c1e-4de57aee748c">IAttachmentExecute::Execute</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>



<a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a>
 

 

