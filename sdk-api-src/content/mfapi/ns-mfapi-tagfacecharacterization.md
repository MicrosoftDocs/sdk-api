---
UID: NS:mfapi.tagFaceCharacterization
title: tagFaceCharacterization
author: windows-driver-content
description: The FaceCharacterization structure describes the blob format for the MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS attribute.
old-location: stream\facecharacterization.htm
old-project: stream
ms.assetid: 8A8F6E06-DA09-4595-BF42-8B905453CCCA
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: FaceCharacterization, FaceCharacterization structure [Streaming Media Devices], mfapi/FaceCharacterization, stream.facecharacterization, tagFaceCharacterization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfapi.h
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
req.typenames: FaceCharacterization
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	FaceCharacterization
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagFaceCharacterization structure


## -description


The <b>FaceCharacterization</b> structure describes the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.


## -struct-fields




### -field BlinkScoreLeft

0 indicates no blink for the left eye, 100 indicates definite blink for the left eye (0 - 100).


### -field BlinkScoreRight

0 indicates no blink for the right eye, 100 indicates definite blink for the right eye (0 - 100).


### -field FacialExpression

A  defined facial expression value.


### -field FacialExpressionScore

0 indicates no such facial expression as identified, 100 indicates definite such facial expression as defined (0 - 100).


## -remarks



The <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute contains the blink and facial expression state for the face ROIs identified in <b>MF_CAPTURE_METADATA_FACEROIS</b>.  For a  device that does not support blink or facial expression detection, this attribute should be omitted.

The facial expressions that can be detected are defined as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define MF_METADATAFACIALEXPRESSION_SMILE             0x00000001</pre>
</td>
</tr>
</table></span></div>
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn927643">FaceCharacterizationBlobHeader</a> and <b>FaceCharacterization</b> structures only describe the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.  The metadata item structure for the face characterizations (<a href="https://msdn.microsoft.com/library/windows/hardware/dn925184">KSCAMERA_METADATA_ITEMHEADER</a> + face characterizations metadata payload) is up to driver and must be 8-byte aligned. 



