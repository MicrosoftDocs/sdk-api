---
UID: NF:dshowasf.IConfigAsfWriter2.SetParam
title: IConfigAsfWriter2::SetParam (dshowasf.h)
description: The SetParam method sets the value of the specified filter configuration parameter.
helpviewer_keywords: ["IConfigAsfWriter2 interface [DirectShow]","SetParam method","IConfigAsfWriter2.SetParam","IConfigAsfWriter2::SetParam","IConfigAsfWriter2SetParam","SetParam","SetParam method [DirectShow]","SetParam method [DirectShow]","IConfigAsfWriter2 interface","dshow.iconfigasfwriter2_setparam","dshowasf/IConfigAsfWriter2::SetParam"]
old-location: dshow\iconfigasfwriter2_setparam.htm
tech.root: dshow
ms.assetid: 0294837c-0cf2-4a05-bef4-16d13864f759
ms.date: 12/05/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],SetParam method, IConfigAsfWriter2.SetParam, IConfigAsfWriter2::SetParam, IConfigAsfWriter2SetParam, SetParam, SetParam method [DirectShow], SetParam method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_setparam, dshowasf/IConfigAsfWriter2::SetParam
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter2::SetParam
 - dshowasf/IConfigAsfWriter2::SetParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.SetParam
---

# IConfigAsfWriter2::SetParam


## -description

The <code>SetParam</code> method sets the value of the specified filter configuration parameter.

## -parameters

### -param dwParam [in]

Specifies the parameter to set,as a member of the <a href="/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)">_AM_ASFWRITERCONFIG_PARAM</a> enumeration.

### -param dwParam1 [in]

Specifies the value to assign to the <i>dwParam</i> parameter.

### -param dwParam2 [out]

Reserved. Must be zero.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2">IConfigAsfWriter2 Interface</a>