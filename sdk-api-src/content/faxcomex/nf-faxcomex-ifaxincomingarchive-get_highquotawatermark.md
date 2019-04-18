---
UID: NF:faxcomex.IFaxIncomingArchive.get_HighQuotaWaterMark
title: IFaxIncomingArchive::get_HighQuotaWaterMark (faxcomex.h)
author: windows-sdk-content
description: The HighQuotaWaterMark property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0g2z.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HighQuotaWaterMark property [Fax Service], HighQuotaWaterMark property [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],HighQuotaWaterMark property, IFaxIncomingArchive.HighQuotaWaterMark, IFaxIncomingArchive.get_HighQuotaWaterMark, IFaxIncomingArchive.put_HighQuotaWaterMark, IFaxIncomingArchive::HighQuotaWaterMark, IFaxIncomingArchive::get_HighQuotaWaterMark, IFaxIncomingArchive::put_HighQuotaWaterMark, _mfax_faxincomingarchive.highquotawatermark, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_highquotawatermark_cpp, fax._mfax_faxincomingarchive_highquotawatermark, faxcomex/IFaxIncomingArchive::HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::get_HighQuotaWaterMark, faxcomex/IFaxIncomingArchive::put_HighQuotaWaterMark, get_HighQuotaWaterMark
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
 - IFaxIncomingArchive.HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
 - IFaxIncomingArchive.get_HighQuotaWaterMark
 - IFaxIncomingArchive.put_HighQuotaWaterMark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingArchive::get_HighQuotaWaterMark


## -description


The <b>HighQuotaWaterMark</b> property is a value that specifies the upper warning threshold for the size of the archive of inbound fax messages, in megabytes. If the size of the archive exceeds this value, and the <a href="https://msdn.microsoft.com/en-us/library/ms685982(v=VS.85).aspx">SizeQuotaWarning</a> property is equal to <b>TRUE</b>, the fax service issues a warning in the event log.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358922(v=VS.85).aspx">IFaxConfiguration::put_HighQuotaWaterMark</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358922(v=VS.85).aspx">IFaxConfiguration::get_HighQuotaWaterMark</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687473(v=VS.85).aspx">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692976(v=VS.85).aspx">Visual Basic Example</a>
 

 

