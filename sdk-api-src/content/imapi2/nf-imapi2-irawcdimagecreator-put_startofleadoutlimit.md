---
UID: NF:imapi2.IRawCDImageCreator.put_StartOfLeadoutLimit
title: IRawCDImageCreator::put_StartOfLeadoutLimit
author: windows-sdk-content
description: Sets the StartOfLeadoutLimit property value.
old-location: imapi\irawcdimagecreator_put_startofleadoutlimit.htm
tech.root: imapi
ms.assetid: e3483084-8339-4fe6-abd1-832832c549f3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],put_StartOfLeadoutLimit method, IRawCDImageCreator.put_StartOfLeadoutLimit, IRawCDImageCreator::put_StartOfLeadoutLimit, imapi.irawcdimagecreator_put_startofleadoutlimit, imapi2/IRawCDImageCreator::put_StartOfLeadoutLimit, put_StartOfLeadoutLimit, put_StartOfLeadoutLimit method [IMAPI], put_StartOfLeadoutLimit method [IMAPI],IRawCDImageCreator interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator.put_StartOfLeadoutLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageCreator::put_StartOfLeadoutLimit


## -description


Sets the <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.<div class="alert"><b>Note</b>  The maximum supported value for this property is 398,099, which equates to MSF 88:29:74. </div>
<div> </div>



## -parameters




### -param value [in]

Pointer to a <b>LONG</b> value that represents the current  <i>StartOfLeadoutLimit</i>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/07397f94-fd32-4507-89dd-53de7f25b231">IRawCDImageCreator::get_StartOfLeadoutLimit</a>
 

 

