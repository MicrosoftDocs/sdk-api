---
UID: NF:mfidl.IMFPMPHostApp.ActivateClassById
title: IMFPMPHostApp::ActivateClassById
author: windows-sdk-content
description: Creates a Windows Runtime object in the protected media path (PMP) process.
old-location: mf\imfpmphostapp_activateclassbyid.htm
tech.root: medfound
ms.assetid: e0e14171-fcc9-418a-a93d-3cdbae254a3f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ActivateClassById, ActivateClassById method [Media Foundation], ActivateClassById method [Media Foundation],IMFPMPHostApp interface, IMFPMPHostApp interface [Media Foundation],ActivateClassById method, IMFPMPHostApp.ActivateClassById, IMFPMPHostApp::ActivateClassById, mf.imfpmphostapp_activateclassbyid, mfidl/IMFPMPHostApp::ActivateClassById
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
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
 - mfidl.h
api_name:
 - IMFPMPHostApp.ActivateClassById
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPHostApp::ActivateClassById


## -description


Creates a Windows Runtime object in the protected media path (PMP) process.
        


## -parameters




### -param id [in]

Id of object to create.


### -param pStream [in]

Data to be passed to the object by way of a <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>.


### -param riid [in]

The interface identifier (IID) of the interface to retrieve.
          


### -param ppv [out]

Receives a pointer to the created object. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a>
 

 

