---
UID: NF:faxcomex.IFaxIncomingArchive.put_UseArchive
title: IFaxIncomingArchive::put_UseArchive (faxcomex.h)
author: windows-sdk-content
description: The UseArchive property is a Boolean value that indicates whether the fax service archives inbound fax messages.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_usearchive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9e5h.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxIncomingArchive interface [Fax Service],UseArchive property, IFaxIncomingArchive.UseArchive, IFaxIncomingArchive.get_UseArchive, IFaxIncomingArchive.put_UseArchive, IFaxIncomingArchive::UseArchive, IFaxIncomingArchive::get_UseArchive, IFaxIncomingArchive::put_UseArchive, UseArchive property [Fax Service], UseArchive property [Fax Service],IFaxIncomingArchive interface, _mfax_faxincomingarchive.usearchive, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_usearchive_cpp, fax._mfax_faxincomingarchive_usearchive, faxcomex/IFaxIncomingArchive::UseArchive, faxcomex/IFaxIncomingArchive::get_UseArchive, faxcomex/IFaxIncomingArchive::put_UseArchive, put_UseArchive
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
 - IFaxIncomingArchive.UseArchive
 - IFaxIncomingArchive.get_UseArchive
 - IFaxIncomingArchive.put_UseArchive
 - IFaxIncomingArchive.get_UseArchive
 - IFaxIncomingArchive.put_UseArchive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::put_UseArchive


## -description


The <b>UseArchive</b> property is a Boolean value that indicates whether the fax service archives inbound fax messages. If this property is equal to <b>TRUE</b>, the fax service archives inbound fax messages. If this property is equal to <b>FALSE</b>, the fax service does not archive inbound faxes.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows,  get the <a href="https://msdn.microsoft.com/en-us/library/ms693549(v=VS.85).aspx">IFaxConfiguration</a> interface from the <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface, and then call the  <a href="https://msdn.microsoft.com/en-us/library/Aa358932(v=VS.85).aspx">IFaxConfiguration::put_UseArchive</a>   or <a href="https://msdn.microsoft.com/en-us/library/Aa358932(v=VS.85).aspx">IFaxConfiguration::get_UseArchive</a> method.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687473(v=VS.85).aspx">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692976(v=VS.85).aspx">Visual Basic Example</a>
 

 

