---
UID: NF:faxcomex.IFaxOutgoingArchive.put_UseArchive
title: IFaxOutgoingArchive::put_UseArchive (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingArchive::get_UseArchive property is a Boolean value that indicates whether the fax service archives outbound fax messages.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_usearchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4pk5.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],UseArchive property, IFaxOutgoingArchive.UseArchive, IFaxOutgoingArchive.get_UseArchive, IFaxOutgoingArchive.put_UseArchive, IFaxOutgoingArchive::UseArchive, IFaxOutgoingArchive::get_UseArchive, IFaxOutgoingArchive::put_UseArchive, UseArchive property [Fax Service], UseArchive property [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.usearchive, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_usearchive_cpp, fax._mfax_faxoutgoingarchive_usearchive, faxcomex/IFaxOutgoingArchive::UseArchive, faxcomex/IFaxOutgoingArchive::get_UseArchive, faxcomex/IFaxOutgoingArchive::put_UseArchive, put_UseArchive
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
 - IFaxOutgoingArchive.UseArchive
 - IFaxOutgoingArchive.get_UseArchive
 - IFaxOutgoingArchive.put_UseArchive
 - IFaxOutgoingArchive.get_UseArchive
 - IFaxOutgoingArchive.put_UseArchive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingArchive::put_UseArchive


## -description


The <b>IFaxOutgoingArchive::get_UseArchive</b> property is a Boolean value that indicates whether the fax service archives outbound fax messages. If this parameter is equal to <b>TRUE</b>, the fax service archives outbound fax messages. If this parameter is equal to <b>FALSE</b>, the fax service does not archive outbound faxes.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358932(v=VS.85).aspx">IFaxConfiguration::put_UseArchive</a>   or <b>IFaxConfiguration::get_UseArchive</b> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693472(v=VS.85).aspx">Visual Basic Example</a>
 

 

