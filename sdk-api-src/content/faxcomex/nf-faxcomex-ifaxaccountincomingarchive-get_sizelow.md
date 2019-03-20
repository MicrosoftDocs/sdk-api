---
UID: NF:faxcomex.IFaxAccountIncomingArchive.get_SizeLow
title: IFaxAccountIncomingArchive::get_SizeLow (faxcomex.h)
author: windows-sdk-content
description: Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.
old-location: fax\_mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizelow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountincomingarchive\sizelow.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxAccountIncomingArchive interface [Fax Service],SizeLow property, IFaxAccountIncomingArchive.SizeLow, IFaxAccountIncomingArchive.get_SizeLow, IFaxAccountIncomingArchive::SizeLow, IFaxAccountIncomingArchive::get_SizeLow, SizeLow property [Fax Service], SizeLow property [Fax Service],IFaxAccountIncomingArchive interface, _mfax_faxaccountincomingarchive.sizelow, fax._mfax_faxaccountincomingarchive_cpp_mfax_faxaccountincomingarchive_sizelow_cpp, fax._mfax_faxaccountincomingarchive_sizelow, faxcomex/IFaxAccountIncomingArchive::SizeLow, faxcomex/IFaxAccountIncomingArchive::get_SizeLow, get_SizeLow
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
 - IFaxAccountIncomingArchive.SizeLow
 - IFaxAccountIncomingArchive.get_SizeLow
 - IFaxAccountIncomingArchive.get_SizeLow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxAccountIncomingArchive::get_SizeLow


## -description


Specifies the low 32-bit value (in bytes) for the size of the archive of inbound fax messages for a particular fax account.

This property is read-only.


## -parameters


## -remarks



Because the archive may exceed 4 GB in size, its size is described using two long values. SizeLow is the low 32-bit value of the archive size. SizeHigh is the high 32-bit value of the archive size. The size of the archive is: SizeLow + 4 GB * SizeHigh.

If both the <b>SizeLow</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa359050(v=VS.85).aspx">SizeHigh</a> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358957(v=VS.85).aspx">FaxAccountIncomingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359046(v=VS.85).aspx">IFaxAccountIncomingArchive</a>
 

 

