---
UID: NF:faxcom.IFaxPorts.get_Count
title: IFaxPorts::get_Count
author: windows-sdk-content
description: The IFaxPorts::get_Count method retrieves the number of fax ports attached to the connected fax server.
old-location: fax\_mfax_ifaxports_get_count.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7rp0.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IFaxPorts interface [Fax Service],get_Count method, IFaxPorts.get_Count, IFaxPorts::get_Count, _mfax_ifaxports_get_count, fax._mfax_ifaxports_get_count, faxcom/IFaxPorts::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxPorts interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPorts.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPorts::get_Count


## -description


The <b>IFaxPorts::get_Count</b> method retrieves the number of fax ports attached to the connected fax server.


## -parameters




### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of fax ports attached to the connected fax server. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>IFaxPorts::get_Count</b> method, a fax client application can call the <a href="https://msdn.microsoft.com/library/ms690813(v=VS.85).aspx">IFaxPorts::get_Item</a> method to retrieve an interface pointer to one or more <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> objects. 




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">GetPorts</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690813(v=VS.85).aspx">IFaxPorts::get_Item</a>
 

 

