---
UID: NF:faxcomex.IFaxOutgoingArchive.get_AgeLimit
title: IFaxOutgoingArchive::get_AgeLimit
author: windows-sdk-content
description: The AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_agelimit_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69mc.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],FaxOutgoingArchive object, FaxOutgoingArchive object [Fax Service],AgeLimit property, FaxOutgoingArchive.AgeLimit, IFaxOutgoingArchive.get_AgeLimit, IFaxOutgoingArchive::get_AgeLimit, _mfax_faxoutgoingarchive.agelimit, fax._mfax_faxoutgoingarchive_agelimit, fax._mfax_faxoutgoingarchive_agelimit_vb, get_AgeLimit
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutgoingArchive.AgeLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingArchive::get_AgeLimit


## -description


The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. The fax service deletes messages from the outbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows, get the  <a href="https://msdn.microsoft.com/en-us/library/Aa358914(v=VS.85).aspx">FaxConfiguration.ArchiveAgeLimit</a> property from the <a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a> object.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/library/ms693472(v=VS.85).aspx">Visual Basic Example</a>
 

 

