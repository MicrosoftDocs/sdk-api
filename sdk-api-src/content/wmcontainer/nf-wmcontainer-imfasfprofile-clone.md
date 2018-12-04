---
UID: NF:wmcontainer.IMFASFProfile.Clone
title: IMFASFProfile::Clone
author: windows-sdk-content
description: Creates a copy of the Advanced Systems Format profile object.
old-location: mf\imfasfprofile_clone.htm
tech.root: medfound
ms.assetid: e91d3d2c-ef08-460e-b6f8-e8eed8df5a67
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],Clone method, IMFASFProfile.Clone, IMFASFProfile::Clone, e91d3d2c-ef08-460e-b6f8-e8eed8df5a67, mf.imfasfprofile_clone, wmcontainer/IMFASFProfile::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFProfile.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile::Clone


## -description



Creates a copy of the Advanced Systems Format profile object.




## -parameters




### -param ppIProfile [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a> interface of the new object. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The cloned object is completely independent of the original.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>
 

 

