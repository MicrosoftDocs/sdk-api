---
UID: NN:mfobjects.IMFAttributes
title: IMFAttributes (mfobjects.h)
description: Provides a generic way to store key/value pairs on an object.
helpviewer_keywords: ["IMFAttributes","IMFAttributes interface [Media Foundation]","IMFAttributes interface [Media Foundation]","described","e12259f4-b631-4d4a-a296-c1cc6334b962","mf.imfattributes","mfobjects/IMFAttributes"]
old-location: mf\imfattributes.htm
tech.root: mf
ms.assetid: e12259f4-b631-4d4a-a296-c1cc6334b962
ms.date: 12/05/2018
ms.keywords: IMFAttributes, IMFAttributes interface [Media Foundation], IMFAttributes interface [Media Foundation],described, e12259f4-b631-4d4a-a296-c1cc6334b962, mf.imfattributes, mfobjects/IMFAttributes
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAttributes
 - mfobjects/IMFAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes
---

# IMFAttributes interface


## -description

Provides a generic way to store key/value pairs on an object. The keys are <b>GUID</b>s, and the values can be any of the following data types: <b>UINT32</b>, <b>UINT64</b>, <b>double</b>, <b>GUID</b>, wide-character string, byte array, or <b>IUnknown</b> pointer. The standard implementation of this interface holds a thread lock while values are added, deleted, or retrieved.

For a list of predefined attribute <b>GUID</b>s, see <a href="/windows/desktop/medfound/media-foundation-attributes">Media Foundation Attributes</a>. Each attribute <b>GUID</b> has an expected data type. The various "set" methods in <b>IMFAttributes</b> do not validate the type against the attribute <b>GUID</b>. It is the application's responsibility to set the correct type for the attribute.

To create an empty attribute store, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a>.

## -inheritance

The <b>IMFAttributes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFAttributes</b> also has these types of members:

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
