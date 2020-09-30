---
UID: NF:iads.IADsPrintQueueOperations.PrintJobs
title: IADsPrintQueueOperations::PrintJobs (iads.h)
description: The IADsPrintQueueOperations::PrintJobs method gets an IADsCollection interface pointer on the collection of the print jobs processed in this print queue.
helpviewer_keywords: ["IADsPrintQueueOperations interface [ADSI]","PrintJobs method","IADsPrintQueueOperations.PrintJobs","IADsPrintQueueOperations::PrintJobs","PrintJobs","PrintJobs method [ADSI]","PrintJobs method [ADSI]","IADsPrintQueueOperations interface","_ds_iadsprintqueueoperations_printjobs","adsi.iadsprintqueueoperations__printjobs","adsi.iadsprintqueueoperations_printjobs","iads/IADsPrintQueueOperations::PrintJobs"]
old-location: adsi\iadsprintqueueoperations_printjobs.htm
tech.root: adsi
ms.assetid: fe92fef3-596f-416c-b613-1d93737c298e
ms.date: 12/05/2018
ms.keywords: IADsPrintQueueOperations interface [ADSI],PrintJobs method, IADsPrintQueueOperations.PrintJobs, IADsPrintQueueOperations::PrintJobs, PrintJobs, PrintJobs method [ADSI], PrintJobs method [ADSI],IADsPrintQueueOperations interface, _ds_iadsprintqueueoperations_printjobs, adsi.iadsprintqueueoperations__printjobs, adsi.iadsprintqueueoperations_printjobs, iads/IADsPrintQueueOperations::PrintJobs
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsPrintQueueOperations::PrintJobs
 - iads/IADsPrintQueueOperations::PrintJobs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPrintQueueOperations.PrintJobs
---

# IADsPrintQueueOperations::PrintJobs


## -description

The <b>IADsPrintQueueOperations::PrintJobs</b> method gets an  <a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a> interface pointer on the collection of the print jobs processed in this print queue. This collection can be enumerated using the standard Automation enumeration methods on  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>. To delete a print job, use the  <a href="/windows/desktop/api/iads/nf-iads-iadscollection-remove">IADsCollection::Remove</a> method on the retrieved interface pointer.

## -parameters

### -param pObject [out]

Pointer to a pointer to the  <a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a> interface on the collection of objects added to this print queue. Objects in the collection implement the  <a href="/windows/desktop/api/iads/nn-iads-iadsprintjob">IADsPrintJob</a> interface.

## -returns

This method supports the standard return values. For more information about other return values, see the  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscollection-remove">IADsCollection::Remove</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsprintjob">IADsPrintJob</a>



<a href="/windows/desktop/ADSI/iadsprintjob-property-methods">IADsPrintJob Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsprintqueueoperations">IADsPrintQueueOperations</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>