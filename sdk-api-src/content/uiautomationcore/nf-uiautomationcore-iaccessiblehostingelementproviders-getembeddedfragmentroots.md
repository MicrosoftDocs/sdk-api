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

# IAccessibleHostingElementProviders::GetEmbeddedFragmentRoots


## -description


Retrieves the  Microsoft Active Accessibility providers of  all windowless Microsoft ActiveX controls that have a Microsoft UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the <a href="https://msdn.microsoft.com/8D974311-25CB-4D49-B907-2984D0DA58D7">IAccessibleHostingElementProviders</a> interface.


## -parameters




### -param pRetVal [out, retval]

Type: <b>SAFEARRAY**</b>

Receives the <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a> interface pointers.  


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The container of windowless ActiveX controls implements this method on the same object that implements the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface.  When called, this method queries each of the contained windowless ActiveX controls for an <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a> pointer, and then adds the pointer to the safe array.  

This method should not include any providers that do not implement <b>IRawElementProviderFragmentRoot</b>. 





## -see-also




<a href="https://msdn.microsoft.com/8D974311-25CB-4D49-B907-2984D0DA58D7">IAccessibleHostingElementProviders</a>
 

 

