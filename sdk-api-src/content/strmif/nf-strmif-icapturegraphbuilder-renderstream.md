---
UID: NF:strmif.ICaptureGraphBuilder.RenderStream
title: ICaptureGraphBuilder::RenderStream
author: windows-sdk-content
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.
old-location: dshow\icapturegraphbuilder_renderstream.htm
tech.root: DirectShow
ms.assetid: 2b174f31-d7bb-4934-9d5b-2e4fd6ae8bf5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICaptureGraphBuilder interface [DirectShow],RenderStream method, ICaptureGraphBuilder.RenderStream, ICaptureGraphBuilder::RenderStream, ICaptureGraphBuilderRenderStream, RenderStream, RenderStream method [DirectShow], RenderStream method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_renderstream, strmif/ICaptureGraphBuilder::RenderStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - ICaptureGraphBuilder.RenderStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptureGraphBuilder::RenderStream


## -description



<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/abdf6fb2-e98f-4df8-98ec-06d33798abb5">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Connects a source filter's pin, of an optionally specified category, to the rendering filter, and optionally through another filter.




## -parameters




### -param pCategory [in]

Pointer to a GUID specifying which output pin of the source filter to connect. See <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a> for a list of all pin categories. <b>NULL</b> indicates render the only output pin, regardless of category.


### -param pSource [in]

Pointer to an <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> or an <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface representing either the source filter or an output pin. Source filters are typically a file source filter, such as an AVI file source filter or a capture filter.


### -param pfCompressor [in]

Pointer to an <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface representing the optional compression filter.


### -param pfRenderer [in]

Pointer to an <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface representing the renderer. You can use the <i>ppf</i> (multiplexer) parameter from <a href="https://msdn.microsoft.com/f410465f-c560-49ab-9194-66d708274f77">ICaptureGraphBuilder::SetOutputFileName</a> to supply this value.


## -returns



Returns VFW_S_NOPREVIEWPIN if the capture filter has a capture pin but no preview pin, and you call <code>RenderStream</code> with the &amp;PIN_CATEGORY_PREVIEW category on the capture pin. In this case, <code>RenderStream</code> will render the preview pin of the <a href="https://msdn.microsoft.com/25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9">Smart Tee</a> filter. For more information, see Remarks.




## -remarks



If you specify a non-<b>NULL</b><a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a> GUID for <i>pCategory</i> and a capture filter for <i>pSource</i>, this method instantiates and connects additional required upstream filters, such as TV tuners and crossbars. It then renders the capture pin of <i>pSource</i>.

If <i>pSource</i> is a pin, then specify <b>NULL</b> for <i>pCategory</i> and this method renders the stream from that pin.

If the source filter has only one output pin, specify <b>NULL</b> for <i>pCategory</i>.

<i>pSource</i>, <i>pfCompressor</i>, and <i>pfRenderer</i> filters given as parameters must be present in the graph before this method is called.

If you are building a capture graph that is using WDM capture filters, this method will build all necessary upstream filters as well as the downstream filters.

Some capture filters that work with new WDM VPE (Video Port Extension) video capture hardware have video port pins instead of preview pins meant for previewing. Video port pins do not connect directly to a video renderer, but instead to a special filter called the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>. Your application does not need to worry about this. All you have to do is call <code>RenderStream</code> with PIN_CATEGORY_PREVIEW and the capture graph builder will correctly render the VIDEO PORT pin through an overlay mixer if that is what is necessary.

When you render a capture or preview pin of a video capture filter (using <code>RenderStream</code> with the PIN_CATEGORY_CAPTURE or PIN_CATEGORY_PREVIEW category) and the capture filter has a capture pin but no preview pin, the <a href="https://msdn.microsoft.com/25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9">Smart Tee</a> filter will be used automatically to allow simultaneous capture and preview. For example, calling <code>RenderStream</code> with the PIN_CATEGORY_CAPTURE category will actually connect a Smart Tee filter to the capture pin of the filter, and then render the capture pin of the Smart Tee. If you then call <code>RenderStream</code> with the PIN_CATEGORY_PREVIEW category on the capture pin, it will actually render the preview pin of the Smart Tee. If calling <code>RenderStream</code> with PIN_CATEGORY_PREVIEW results in using the capture pin and a Smart Tee filter, <code>RenderStream</code> will return VFW_S_NOPREVIEWPIN to indicate this. Thus, if <a href="https://msdn.microsoft.com/23fe9a5a-0f3b-44b3-9d37-6889214657bf">FindInterface</a> fails to find a preview interface, you may need to call <b>FindInterface</b> with the PIN_CATEGORY_PREVIEW category and with the PIN_CATEGORY_CAPTURE category, because the preview interface can be found by looking downstream of the capture pin of the capture filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/64ee80cd-9f63-4f38-853a-1ecfc03e6076">ICaptureGraphBuilder Interface</a>
 

 

