---
UID: NS:comsvcs.__MIDL___MIDL_itf_autosvcs_0000_0013_0001
title: COMSVCSEVENTINFO (comsvcs.h)
description: Represents contextual information about an event, such as the time it was generated and which process server and COM+ application generated it.
helpviewer_keywords: ["COMSVCSEVENTINFO","COMSVCSEVENTINFO structure [COM+]","_dtc_Event_Structure","comsvcs/COMSVCSEVENTINFO","cos.comsvcseventinfo"]
old-location: cos\comsvcseventinfo.htm
tech.root: cos
ms.assetid: f4aa0892-4c93-42ea-adc6-1b304b917389
ms.date: 12/05/2018
ms.keywords: COMSVCSEVENTINFO, COMSVCSEVENTINFO structure [COM+], _dtc_Event_Structure, comsvcs/COMSVCSEVENTINFO, cos.comsvcseventinfo
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMSVCSEVENTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_autosvcs_0000_0013_0001
 - comsvcs/__MIDL___MIDL_itf_autosvcs_0000_0013_0001
 - COMSVCSEVENTINFO
 - comsvcs/COMSVCSEVENTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - COMSVCSEVENTINFO
---

# COMSVCSEVENTINFO structure


## -description

Represents contextual information about an event, such as the time it was generated and which process server and COM+ application generated it.

## -struct-fields

### -field cbSize

The size of this structure, in bytes.

### -field dwPid

The process ID of the server application from which the event originated.

### -field lTime

The coordinated universal time of the event, as seconds elapsed since midnight, January 1, 1970.

### -field lMicroTime

The microseconds added to <b>lTime</b> for time to microsecond resolution.

### -field perfCount

The value of the high-resolution performance counter when the event originated.

### -field guidApp

The applications globally unique identifier (GUID) for the first component instantiated in <b>dwPid</b>. If you are subscribing to an administration interface or event and the event is not generated from a COM+ application, this member is set to zero.

### -field sMachineName

The fully qualified name of the computer where the event originated.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomactivityevents">IComActivityEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomapp2events">IComApp2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomappevents">IComAppEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomexceptionevents">IComExceptionEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomidentityevents">IComIdentityEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstance2events">IComInstance2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icominstanceevents">IComInstanceEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomltxevents">IComLTxEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethod2events">IComMethod2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icommethodevents">IComMethodEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectconstruction2events">IComObjectConstruction2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectconstructionevents">IComObjectConstructionEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectevents">IComObjectEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpool2events">IComObjectPool2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents">IComObjectPoolEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomobjectpoolevents2">IComObjectPoolEvents2</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomresourceevents">IComResourceEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomsecurityevents">IComSecurityEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomthreadevents">IComThreadEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfoevents">IComTrackingInfoEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransactionevents">IComTransactionEvents</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomuserevent">IComUserEvent</a>