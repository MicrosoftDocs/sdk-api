---
UID: NF:msinkaut.IInkRecognizer.get_PreferredPacketDescription
title: IInkRecognizer::get_PreferredPacketDescription (msinkaut.h)
description: Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer.
helpviewer_keywords: ["3486f667-a050-4063-99bf-09865d6edbda","IInkRecognizer interface [Tablet PC]","PreferredPacketDescription property","IInkRecognizer.PreferredPacketDescription","IInkRecognizer.get_PreferredPacketDescription","IInkRecognizer::PreferredPacketDescription","IInkRecognizer::get_PreferredPacketDescription","PreferredPacketDescription property [Tablet PC]","PreferredPacketDescription property [Tablet PC]","IInkRecognizer interface","get_PreferredPacketDescription","msinkaut/IInkRecognizer::PreferredPacketDescription","msinkaut/IInkRecognizer::get_PreferredPacketDescription","tablet.iinkrecognizer_preferredpacketdescription"]
old-location: tablet\iinkrecognizer_preferredpacketdescription.htm
tech.root: tablet
ms.assetid: 3486f667-a050-4063-99bf-09865d6edbda
ms.date: 12/05/2018
ms.keywords: 3486f667-a050-4063-99bf-09865d6edbda, IInkRecognizer interface [Tablet PC],PreferredPacketDescription property, IInkRecognizer.PreferredPacketDescription, IInkRecognizer.get_PreferredPacketDescription, IInkRecognizer::PreferredPacketDescription, IInkRecognizer::get_PreferredPacketDescription, PreferredPacketDescription property [Tablet PC], PreferredPacketDescription property [Tablet PC],IInkRecognizer interface, get_PreferredPacketDescription, msinkaut/IInkRecognizer::PreferredPacketDescription, msinkaut/IInkRecognizer::get_PreferredPacketDescription, tablet.iinkrecognizer_preferredpacketdescription
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizer::get_PreferredPacketDescription
 - msinkaut/IInkRecognizer::get_PreferredPacketDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer.PreferredPacketDescription
 - IInkRecognizer.get_PreferredPacketDescription
 - IInkRecognizer.get_PreferredPacketDescription
---

# IInkRecognizer::get_PreferredPacketDescription


## -description

Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer.



This property is read-only.

## -parameters

## -remarks

This property describes the contents of a packet and does not allow access to the data that the packet contains.

This property lists the packet properties that the recognizer uses to complete recognition. For all of the Microsoft recognizers, the <b>PreferredPacketDescription</b> property refers to the data describing (x, y) coordinates within an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object. This data is represented by the X and Y fields of the <a href="/windows/desktop/tablet/packetpropertyguids-constants">packet property</a> constants. A packet contains this point data as well as other data that is related to that stroke, such as the pressure of the pen that made the stroke, the angle of the pen, and so on. The Microsoft recognizers ignore pressure, tilt, and other packet properties.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>