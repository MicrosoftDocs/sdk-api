---
UID: NF:faxcomex.IFaxSecurity2.Refresh
title: IFaxSecurity2::Refresh
author: windows-sdk-content
description: Refreshes FaxSecurity2 object information from the fax server.
old-location: fax\_mfax_faxsecurity2_cpp_mfax_faxsecurity2_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\refresh.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxSecurity2 interface [Fax Service],Refresh method, IFaxSecurity2.Refresh, IFaxSecurity2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxSecurity2 interface, _mfax_faxsecurity2.refresh, fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_refresh_cpp, fax._mfax_faxsecurity2_refresh, faxcomex/IFaxSecurity2::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
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
 - IFaxSecurity2.Refresh
 - IFaxSecurity2.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSecurity2::Refresh


## -description


Refreshes <a href="https://msdn.microsoft.com/213e555a-1509-4081-a21b-f33fc4653f32">FaxSecurity2</a> object information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <b>IFaxSecurity2::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/7ae27584-956c-464a-8c0c-48b06ac9e309">IFaxSecurity2::Save</a> method call are lost.

To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/213e555a-1509-4081-a21b-f33fc4653f32">FaxSecurity2</a>



<a href="https://msdn.microsoft.com/a6238a8f-3e19-4dd8-b602-525774d671df">IFaxSecurity2</a>
 

 

