---
UID: NS:oaidl.tagEXCEPINFO
title: EXCEPINFO (oaidl.h)
description: Describes an exception that occurred during IDispatch::Invoke.
helpviewer_keywords: ["*LPEXCEPINFO","EXCEPINFO","EXCEPINFO structure [Automation]","LPEXCEPINFO","LPEXCEPINFO structure pointer [Automation]","_oa96_EXCEPINFO","automat.excepinfo","oaidl/EXCEPINFO","oaidl/LPEXCEPINFO"]
old-location: automat\excepinfo.htm
tech.root: automat
ms.assetid: 29583e58-10a6-4679-a5c6-d51f2b50b074
ms.date: 12/05/2018
ms.keywords: '*LPEXCEPINFO, EXCEPINFO, EXCEPINFO structure [Automation], LPEXCEPINFO, LPEXCEPINFO structure pointer [Automation], _oa96_EXCEPINFO, automat.excepinfo, oaidl/EXCEPINFO, oaidl/LPEXCEPINFO'
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: EXCEPINFO, *LPEXCEPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEXCEPINFO
 - oaidl/tagEXCEPINFO
 - LPEXCEPINFO
 - oaidl/LPEXCEPINFO
 - EXCEPINFO
 - oaidl/EXCEPINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - EXCEPINFO
---

# EXCEPINFO structure


## -description

Describes an exception that occurred during <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a>.

## -struct-fields

### -field wCode

The error code. Error codes should be greater than 1000. Either this field or the scode field must be filled in; the other must be set to 0.

### -field wReserved

Reserved. Should be 0.

### -field bstrSource

The name of the exception source. Typically, this is an application name. This field should be filled in by the implementer of <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>.

### -field bstrDescription

The exception description to display. If no description is available, use null.

### -field bstrHelpFile

The fully qualified help file path. If no Help is available, use null.

### -field dwHelpContext

The help context ID.

### -field pvReserved

Reserved. Must be null.

### -field pfnDeferredFillIn

Provides deferred fill-in. If deferred fill-in is not desired, this field should be set to null.

### -field scode

A return value that describes the error. Either this field or wCode (but not both) must be filled in; the other must be set to 0. (16-bit Windows versions only.)

## -remarks

Use the <b>pfnDeferredFillIn</b> field to enable an object to defer filling in the <b>bstrDescription</b>, <b>bstrHelpFile</b>, and <b>dwHelpContext</b> fields until they are needed. This field might be used, for example, if loading the string for the error is a time-consuming operation. To use deferred fill-in, the object puts a function pointer in this slot and does not fill any of the other fields except <b>wCode</b>, which is required.

To get additional information, the caller passes the <b>EXCEPINFO</b> structure back to the <b>pexcepinfo</b> callback function, which fills in the additional information. When the ActiveX object and the ActiveX client are in different processes, the ActiveX object calls <b>pfnDeferredFillIn</b> before returning to the controller.