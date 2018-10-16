---
UID: NF:faxcomex.IFaxDeviceProviders.get__NewEnum
title: IFaxDeviceProviders::get__NewEnum
author: windows-sdk-content
description: The IFaxDeviceProviders::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxDeviceProviders collection.
old-location: fax\_mfax_ifaxdeviceproviders_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0u25.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxDeviceProviders interface [Fax Service],get__NewEnum method, IFaxDeviceProviders.get__NewEnum, IFaxDeviceProviders::get__NewEnum, _mfax_ifaxdeviceproviders_get__newenum, fax._mfax_ifaxdeviceproviders_get__newenum, faxcomex/IFaxDeviceProviders::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxDeviceProviders interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDeviceProviders.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDeviceProviders::get__NewEnum


## -description


The <b>IFaxDeviceProviders::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="_com_IUnknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="_com_IUnknown">IUnknown</a> interface for the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, you do not need to use the <b>_NewEnum</b> property, because it is automatically used in the implementation of <b>For Each ... Next</b>.




## -see-also




<a href="https://msdn.microsoft.com/3abb80d7-fedf-469d-b17a-604ca78f4b8b">FaxDeviceProviders</a>



<a href="https://msdn.microsoft.com/6c1bd4dd-a2bb-4ae7-a719-ec4506065c41">IFaxDeviceProviders</a>
 

 

