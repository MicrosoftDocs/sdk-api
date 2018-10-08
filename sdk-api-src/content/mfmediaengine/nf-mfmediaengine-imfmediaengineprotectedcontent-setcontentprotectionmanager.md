---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetContentProtectionManager
title: IMFMediaEngineProtectedContent::SetContentProtectionManager
author: windows-sdk-content
description: Sets the content protection manager (CPM).
old-location: mf\imfmediaengineprotectedcontent_setcontentprotectionmanager.htm
tech.root: medfound
ms.assetid: 8F150CB5-43AB-4709-A254-636440113642
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetContentProtectionManager method, IMFMediaEngineProtectedContent.SetContentProtectionManager, IMFMediaEngineProtectedContent::SetContentProtectionManager, SetContentProtectionManager, SetContentProtectionManager method [Media Foundation], SetContentProtectionManager method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setcontentprotectionmanager, mfmediaengine/IMFMediaEngineProtectedContent::SetContentProtectionManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetContentProtectionManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineProtectedContent::SetContentProtectionManager


## -description


Sets the content protection manager (CPM).


## -parameters




### -param pCPM [in]

A pointer to the <a href="https://msdn.microsoft.com/0dba0384-eac7-456a-af9f-86eb944cdb2e">IMFContentProtectionManager</a> interface, implemented by the caller.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Media Engine uses the CPM to handle events related to protected content, such as license acquisition.




## -see-also




<a href="https://msdn.microsoft.com/85B37711-DB46-4BC7-A051-79E9507791FA">IMFMediaEngineProtectedContent</a>
 

 

