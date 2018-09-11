---
UID: NF:faxcomex.IFaxDevice.Refresh
title: IFaxDevice::Refresh
author: windows-sdk-content
description: The IFaxDevice::Refresh method refreshes FaxDevice object information from the fax server. When the IFaxDevice::Refresh method is called, any configuration changes made after the last IFaxDevice::Save method call are lost.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6ka0.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxDevice interface [Fax Service],Refresh method, IFaxDevice.Refresh, IFaxDevice::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxDevice interface, _mfax_faxdevice.refresh, fax._mfax_faxdevice_cpp_mfax_faxdevice_refresh_cpp, fax._mfax_faxdevice_refresh, faxcomex/IFaxDevice::Refresh
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
 - IFaxDevice.Refresh
 - IFaxDevice.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::Refresh


## -description


The <b>IFaxDevice::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object information from the fax server. When the <b>IFaxDevice::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/16183ae9-0bfc-4717-867b-88dd3eb7c9ff">IFaxDevice::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

