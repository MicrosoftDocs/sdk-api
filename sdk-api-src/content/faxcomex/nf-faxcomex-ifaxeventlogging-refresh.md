---
UID: NF:faxcomex.IFaxEventLogging.Refresh
title: IFaxEventLogging::Refresh
author: windows-sdk-content
description: The IFaxEventLogging::Refresh method refreshes IFaxEventLogging interface information from the fax server.
old-location: fax\_mfax_faxeventlogging_cpp_mfax_faxeventlogging_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_7ns8.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxEventLogging interface [Fax Service],Refresh method, IFaxEventLogging.Refresh, IFaxEventLogging::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxEventLogging interface, _mfax_faxeventlogging.refresh, fax._mfax_faxeventlogging_cpp_mfax_faxeventlogging_refresh_cpp, fax._mfax_faxeventlogging_refresh, faxcomex/IFaxEventLogging::Refresh
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
 - IFaxEventLogging.Refresh
 - IFaxEventLogging.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxEventLogging::Refresh


## -description


The <b>IFaxEventLogging::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/8acf484d-82c8-477e-bc05-83a0202a42c8">IFaxEventLogging</a> interface information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <a href="https://msdn.microsoft.com/c46f1b55-8211-4c9b-a622-356f2ea2db36">FaxEventLogging</a> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/04783d57-a568-4848-b563-a8ef8544089d">IFaxEventLogging::Save</a> method call are lost.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/c46f1b55-8211-4c9b-a622-356f2ea2db36">FaxEventLogging</a>



<a href="https://msdn.microsoft.com/8acf484d-82c8-477e-bc05-83a0202a42c8">IFaxEventLogging</a>



<a href="https://msdn.microsoft.com/afee6ea0-f63d-4818-9ff0-1887638d232c">Visual Basic Example</a>
 

 

