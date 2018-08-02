---
UID: NF:faxcom.IFaxTiff.get_RawReceiveTime
title: IFaxTiff::get_RawReceiveTime
author: windows-sdk-content
description: Retrieves the RawReceiveTime property for a FaxTiff object.
old-location: fax\_mfax_ifaxtiff_get_rawreceivetime_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9usl.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxTiff object [Fax Service],RawReceiveTime property, FaxTiff.RawReceiveTime, IFaxTiff.get_RawReceiveTime, IFaxTiff::get_RawReceiveTime, RawReceiveTime property [Fax Service], RawReceiveTime property [Fax Service],FaxTiff object, _mfax_ifaxtiff_get_rawreceivetime, fax._mfax_ifaxtiff_get_rawreceivetime, fax._mfax_ifaxtiff_get_rawreceivetime_vb, get_RawReceiveTime
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
 - FaxTiff.RawReceiveTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxTiff::get_RawReceiveTime


## -description


Retrieves the <b>RawReceiveTime</b> property for a <a href="https://msdn.microsoft.com/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>RawReceiveTime</b> property is the time at which reception began for an inbound fax file, expressed in Coordinated Universal Time (UTC). This property can also be the time at which reception or transmission began for an archived file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/en-us/library/ms690773(v=VS.85).aspx">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>get_RawReceiveTime</b> method sets the <i>pVal</i> parameter to the local time at which the fax job started receiving or transmitting the fax file. 

The <b>RawReceiveTime</b> property contains the local time at which the fax job started receiving or transmitting the fax file. 

The <a href="https://msdn.microsoft.com/en-us/library/ms691929(v=VS.85).aspx">get_ReceiveTime</a> method returns the time in a formatted string.

The <a href="https://msdn.microsoft.com/en-us/library/ms691929(v=VS.85).aspx">ReceiveTime</a> property contains the time in a formatted string.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690285(v=VS.85).aspx">FaxTiff</a>



<a href="https://msdn.microsoft.com/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690773(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691929(v=VS.85).aspx">ReceiveTime</a>
 

 

