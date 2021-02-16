---
UID: NF:rtscom.IStrokeBuilder.EndStroke
title: IStrokeBuilder::EndStroke (rtscom.h)
description: Ends a stroke and returns the stroke object.
helpviewer_keywords: ["EndStroke","EndStroke method [Tablet PC]","EndStroke method [Tablet PC]","IStrokeBuilder interface","IStrokeBuilder interface [Tablet PC]","EndStroke method","IStrokeBuilder.EndStroke","IStrokeBuilder::EndStroke","a535cd20-d24a-4044-a757-fb2b593650b9","rtscom/IStrokeBuilder::EndStroke","tablet.istrokebuilder_endstroke"]
old-location: tablet\istrokebuilder_endstroke.htm
tech.root: tablet
ms.assetid: a535cd20-d24a-4044-a757-fb2b593650b9
ms.date: 12/05/2018
ms.keywords: EndStroke, EndStroke method [Tablet PC], EndStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],EndStroke method, IStrokeBuilder.EndStroke, IStrokeBuilder::EndStroke, a535cd20-d24a-4044-a757-fb2b593650b9, rtscom/IStrokeBuilder::EndStroke, tablet.istrokebuilder_endstroke
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStrokeBuilder::EndStroke
 - rtscom/IStrokeBuilder::EndStroke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStrokeBuilder.EndStroke
---

# IStrokeBuilder::EndStroke


## -description

Ends a stroke and returns the stroke object.

## -parameters

### -param tcid [in]

The tablet context identifier.

### -param sid [in]

The stylus identifier.

### -param ppIInkStroke [in, out]

A pointer to the new stroke. This value can be <b>NULL</b>.

### -param pDirtyRect [in, out]

The dirty, or changed, rectangle of the tablet. This value can be <b>NULL</b>.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>..

## -remarks

A dirty region describes a tablet range which has been changed.


#### Examples

The following C++ example shows the implementation of a <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">IStylusPlugin::StylusUp Method</a> method on an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a> object. The plug-in uses a <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::EndStroke Method</b> method is called from <b>IStylusPlugin::StylusUp Method</b> to complete the construction of the stroke and add it to the <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-get_ink">Ink</a> object of the <b>StrokeBuilder Class</b>.


```cpp
STDMETHODIMP CStrokeBuilderPlugin::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
    // Finish the stroke. This adds the stroke to the StrokeBuilder's Ink object.
    return m_pStrokeBuilder->EndStroke(pStylusInfo->tcid, pStylusInfo->cid, &m_piStroke, NULL);
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-appendpackets">IStrokeBuilder::AppendPackets Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-beginstroke">IStrokeBuilder::BeginStroke Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-createstroke">IStrokeBuilder::CreateStroke Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a>