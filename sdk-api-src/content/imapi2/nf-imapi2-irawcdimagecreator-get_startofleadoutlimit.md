---
UID: NF:imapi2.IRawCDImageCreator.get_StartOfLeadoutLimit
title: IRawCDImageCreator::get_StartOfLeadoutLimit
author: windows-driver-content
description: Retrieves the current StartOfLeadoutLimit property value. This value specifies if the resulting image is required to fit on a piece of media with a StartOfLeadout greater than or equal to the LBA.
old-location: imapi\irawcdimagecreator_get_startofleadoutlimit.htm
old-project: imapi
ms.assetid: 07397f94-fd32-4507-89dd-53de7f25b231
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_StartOfLeadoutLimit method, IRawCDImageCreator.get_StartOfLeadoutLimit, IRawCDImageCreator::get_StartOfLeadoutLimit, get_StartOfLeadoutLimit, get_StartOfLeadoutLimit method [IMAPI], get_StartOfLeadoutLimit method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_startofleadoutlimit, imapi2/IRawCDImageCreator::get_StartOfLeadoutLimit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IRawCDImageCreator.get_StartOfLeadoutLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IRawCDImageCreator::get_StartOfLeadoutLimit


## -description


Retrieves the current <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA.


## -parameters




### -param value [out]

Pointer to a <b>LONG</b> value that represents the current  <i>StartOfLeadoutLimit</i>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/e3483084-8339-4fe6-abd1-832832c549f3">IRawCDImageCreator::put_StartOfLeadoutLimit</a>
 

 

