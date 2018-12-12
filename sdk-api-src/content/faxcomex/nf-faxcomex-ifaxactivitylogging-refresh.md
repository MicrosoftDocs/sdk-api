---
UID: NF:faxcomex.IFaxActivityLogging.Refresh
title: IFaxActivityLogging::Refresh
author: windows-sdk-content
description: The IFaxActivityLogging::Refresh method refreshes FaxActivityLogging object information from the fax server.
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1gko.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],Refresh method, IFaxActivityLogging.Refresh, IFaxActivityLogging::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.refresh, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_refresh_cpp, fax._mfax_faxactivitylogging_refresh, faxcomex/IFaxActivityLogging::Refresh
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
 - IFaxActivityLogging.Refresh
 - IFaxActivityLogging.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxActivityLogging::Refresh


## -description


The <b>IFaxActivityLogging::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a> object information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <b>IFaxActivityLogging::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms685941(v=VS.85).aspx">IFaxActivityLogging::Save</a> method call are lost.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684576(v=VS.85).aspx">FaxActivityLogging</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684577(v=VS.85).aspx">IFaxActivityLogging</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693401(v=VS.85).aspx">Visual Basic Example</a>
 

 

