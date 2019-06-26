---
UID: NF:faxcomex.IFaxDevice.Refresh
title: IFaxDevice::Refresh (faxcomex.h)
author: windows-sdk-content
description: The IFaxDevice::Refresh method refreshes FaxDevice object information from the fax server. When the IFaxDevice::Refresh method is called, any configuration changes made after the last IFaxDevice::Save method call are lost.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6ka0.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],Refresh method, IFaxDevice.Refresh, IFaxDevice::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxDevice interface, _mfax_faxdevice.refresh, fax._mfax_faxdevice_cpp_mfax_faxdevice_refresh_cpp, fax._mfax_faxdevice_refresh, faxcomex/IFaxDevice::Refresh
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxDevice.Refresh"
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
ms.custom: 19H1
---

# IFaxDevice::Refresh


## -description


The <b>IFaxDevice::Refresh</b> method refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object information from the fax server. When the <b>IFaxDevice::Refresh</b> method is called, any configuration changes made after the last <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice-save-vb">IFaxDevice::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-the-fax-device-collection">Visual Basic Example</a>
 

 

