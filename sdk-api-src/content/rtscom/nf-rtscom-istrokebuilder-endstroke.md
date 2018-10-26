---
UID: NF:rtscom.IStrokeBuilder.EndStroke
title: IStrokeBuilder::EndStroke
author: windows-sdk-content
description: Ends a stroke and returns the stroke object.
old-location: tablet\istrokebuilder_endstroke.htm
tech.root: tablet
ms.assetid: a535cd20-d24a-4044-a757-fb2b593650b9
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: EndStroke, EndStroke method [Tablet PC], EndStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],EndStroke method, IStrokeBuilder.EndStroke, IStrokeBuilder::EndStroke, a535cd20-d24a-4044-a757-fb2b593650b9, rtscom/IStrokeBuilder::EndStroke, tablet.istrokebuilder_endstroke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStrokeBuilder.EndStroke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>..




## -remarks



A dirty region describes a tablet range which has been changed.


#### Examples

The following C++ example shows the implementation of a <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a> method on an <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a> object. The plug-in uses a <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::EndStroke Method</b> method is called from <b>IStylusPlugin::StylusUp Method</b> to complete the construction of the stroke and add it to the <a href="https://msdn.microsoft.com/ceb8eaea-5059-4386-ad48-63d563ef9731">Ink</a> object of the <b>StrokeBuilder Class</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CStrokeBuilderPlugin::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
    // Finish the stroke. This adds the stroke to the StrokeBuilder's Ink object.
    return m_pStrokeBuilder-&gt;EndStroke(pStylusInfo-&gt;tcid, pStylusInfo-&gt;cid, &amp;m_piStroke, NULL);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder</a>



<a href="https://msdn.microsoft.com/7b53a9b2-11da-4063-aac3-a85e52abeb52">IStrokeBuilder::AppendPackets Method</a>



<a href="https://msdn.microsoft.com/40b8ce05-0272-4505-8361-13bb6ca701ea">IStrokeBuilder::BeginStroke Method</a>



<a href="https://msdn.microsoft.com/f7c6f177-3d89-4f27-b2c0-937b08591305">IStrokeBuilder::CreateStroke Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>
 

 

