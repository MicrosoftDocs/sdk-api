---
UID: NF:faxcomex.IFaxOutgoingArchive.put_AgeLimit
title: IFaxOutgoingArchive::put_AgeLimit method
author: windows-driver-content
description: The AgeLimit property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes.
old-location: fax\_mfax_faxoutgoingarchive_agelimit_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69mc.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: AgeLimit property [Fax Service], AgeLimit property [Fax Service], FaxOutgoingArchive object, FaxOutgoingArchive object [Fax Service], AgeLimit property, IFaxOutgoingArchive, IFaxOutgoingArchive::put_AgeLimit, _mfax_faxoutgoingarchive.agelimit, fax._mfax_faxoutgoingarchive_agelimit, fax._mfax_faxoutgoingarchive_agelimit_vb, put_AgeLimit,IFaxOutgoingArchive.put_AgeLimit
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	FaxOutgoingArchive.AgeLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingArchive::put_AgeLimit method


## -description


The <b>AgeLimit</b> property is a value that indicates the number of days that the fax service retains fax messages in the archive of outbound faxes. The fax service deletes messages from the outbound archive when they exceed the age limit. If the value of this property is zero, the fax service does not enforce an age limit.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  This property is not supported in Windows Vista, Windows Server 2008, and later versions of Windows. To access this property in Windows Vista, Windows Server 2008, and later versions of Windows, get the  <a href="https://msdn.microsoft.com/a8fcdfca-1989-408b-919b-086a15345b4e">FaxConfiguration.ArchiveAgeLimit</a> property from the <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object.</div>
<div> </div>
To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/68f6c0f2-ea06-401c-9021-c50940f8cd7a">Visual Basic Example</a>
 

 

