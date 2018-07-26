---
UID: NF:faxcomex.IFaxIncomingArchive.put_AgeLimit
title: IFaxIncomingArchive::put_AgeLimit
author: windows-sdk-content
description: The AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes.
old-location: fax\_mfax_faxincomingarchive_agelimit_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6vjo.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service],FaxIncomingArchive object, FaxIncomingArchive object [Fax Service],AgeLimit property, FaxIncomingArchive.AgeLimit, IFaxIncomingArchive.put_AgeLimit, IFaxIncomingArchive::put_AgeLimit, _mfax_faxincomingarchive.agelimit, fax._mfax_faxincomingarchive_agelimit, fax._mfax_faxincomingarchive_agelimit_vb, put_AgeLimit
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
 - FaxIncomingArchive.AgeLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingArchive::put_AgeLimit


## -description


The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of inbound faxes. The fax service deletes messages from the inbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows, get the  <a href="https://msdn.microsoft.com/a8fcdfca-1989-408b-919b-086a15345b4e">FaxConfiguration.ArchiveAgeLimit</a> property from the <a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a> object.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms687473(v=VS.85).aspx">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/library/ms687474(v=VS.85).aspx">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/library/ms692976(v=VS.85).aspx">Visual Basic Example</a>
 

 

