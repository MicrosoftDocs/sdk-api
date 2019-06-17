---
UID: NF:prnasnot.IPrintAsyncNotifyDataObject.ReleaseData
title: IPrintAsyncNotifyDataObject::ReleaseData (prnasnot.h)
author: windows-sdk-content
description: Releases the memory used by the data encapsulated in IPrintAsyncNotifyDataObject.
old-location: gdi\iprintasyncnotifydataobject_iprintasyncnotifydataobject__releasedata.htm
tech.root: printdocs
ms.assetid: f4960aa1-237f-491e-b69c-0aa107d9ddad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPrintAsyncNotifyDataObject interface [Windows GDI],ReleaseData method, IPrintAsyncNotifyDataObject.ReleaseData, IPrintAsyncNotifyDataObject::ReleaseData, ReleaseData, ReleaseData method [Windows GDI], ReleaseData method [Windows GDI],IPrintAsyncNotifyDataObject interface, _win32_IPrintAsyncNotifyDataObject_ReleaseData, gdi.iprintasyncnotifydataobject_iprintasyncnotifydataobject__releasedata, prnasnot/IPrintAsyncNotifyDataObject::ReleaseData
ms.topic: method
f1_keywords: ["prnasnot/IPrintAsyncNotifyDataObject.ReleaseData"]
req.header: prnasnot.h
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
req.dll: Prnasnot.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - prnasnot.dll
api_name:
 - IPrintAsyncNotifyDataObject.ReleaseData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrintAsyncNotifyDataObject::ReleaseData


## -description


Releases the memory used by the data encapsulated in <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a>.


## -parameters






## -returns



See <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror">PrintAsyncNotifyError</a> for the possible values.

For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/SetupApi/error-handling">Error Handling</a>.




## -remarks



Listening applications must call this method when they have finished consuming the notification data.

The <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a> interface must be implemented in a way that ensures that a call of <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> does not free the object if a listening application has not finished consuming the object's data. Accordingly, if a call to <b>Release</b> occurs when an application has called <a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata">AcquireData</a> but has not yet called <b>ReleaseData</b>, then the object must not be freed. For this reason, we recommend that <b>AcquireData</b> use <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> to increment the object's reference count, and that <b>ReleaseData</b> decrement the count.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/printdocs/asynchronous-notification-interfaces">Asynchronous Printing Notification Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject">IPrintAsyncNotifyDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/printdocs/printdocs-printing">Printing</a>
 

 

