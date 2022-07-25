---
UID: NN:pnpxassoc.IPNPXDeviceAssociation
title: IPNPXDeviceAssociation (pnpxassoc.h)
description: Defines methods to manage the association database entries for PnP-X devices. These methods send notifications when the corresponding PnP devnode changes.
helpviewer_keywords: ["IPNPXDeviceAssociation","IPNPXDeviceAssociation interface","IPNPXDeviceAssociation interface","described","ncd.ipnpxdeviceassociation","pnpxassoc/IPNPXDeviceAssociation"]
old-location: ncd\ipnpxdeviceassociation.htm
tech.root: ncd
ms.assetid: 52669dec-2fd7-4f3e-b322-e93d9da5984d
ms.date: 12/05/2018
ms.keywords: IPNPXDeviceAssociation, IPNPXDeviceAssociation interface, IPNPXDeviceAssociation interface,described, ncd.ipnpxdeviceassociation, pnpxassoc/IPNPXDeviceAssociation
req.header: pnpxassoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPNPXDeviceAssociation
 - pnpxassoc/IPNPXDeviceAssociation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - pnpxassoc.h
api_name:
 - IPNPXDeviceAssociation
---

# IPNPXDeviceAssociation interface


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Defines methods to manage the association database entries for  PnP-X devices. These methods send notifications when the corresponding PnP devnode changes. An application calls <b>IPNPXDeviceAssociation</b> methods when the application programmatically manages PnP-X device association, either through a custom user interface or through some other method. Usually, the <b>Network Explorer</b> is used to manage PnP-X device association.

## -inheritance

The <b>IPNPXDeviceAssociation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPNPXDeviceAssociation</b> also has these types of members:

## -remarks

This interface is obtained by calling <a href="/previous-versions/windows/desktop/legacy/aa364381(v=vs.85)">QueryService</a> on a function instance returned by a Function Discovery query. The following pseudocode shows the parameters to use for the  <b>QueryService</b> call.


``` syntax
QueryService( SID_PNPXAssociation, __uuidof( IPNPXDeviceAssociation ) )
```

The <b>IPNPXDeviceAssociation</b> methods modify the association database entry for the function instance upon which <a href="/previous-versions/windows/desktop/legacy/aa364381(v=vs.85)">QueryService</a>  was called.

Not all function instances can be associated using the <b>IPNPXDeviceAssociation</b> methods. The function instance must have its  PKEY_PNPX_GlobalIdentity key populated with the UUID supplied by the Function Discovery provider used to discover the device. For more information about property keys, see <a href="/previous-versions/windows/desktop/fundisc/pnp-x-provider-pkeys">PnP-X Provider PKEYs</a>.

## -see-also

<a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxassociation">IPNPXAssociation</a>
