---
UID: TP:tablet
ms.assetid: 8f8b94e8-8687-3dab-9a34-5a6464070552
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Tablet PC

## -description

Overview of the Tablet PC technology.

To develop Tablet PC, you need these headers:

 * [inked.h](..\inked\index.md)
 * [micaut.h](..\micaut\index.md)
 * [msinkaut.h](..\msinkaut\index.md)
 * [msinkaut15.h](..\msinkaut15\index.md)
 * [peninputpanel.h](..\peninputpanel\index.md)
 * [recapis.h](..\recapis\index.md)
 * [rectypes.h](..\rectypes\index.md)
 * [rtscom.h](..\rtscom\index.md)
 * [tabflicks.h](..\tabflicks\index.md)
 * [tpcshrd.h](..\tpcshrd\index.md)

For the programming guide, see [Tablet PC](/windows/desktop/tablet).

## Functions

| Title   | Description   |
| ---- |:---- |
| [AddStroke function](..\recapis\nf-recapis-addstroke.md) | Adds an ink stroke to the RecognizerContext. |
| [AddWordsToWordList function](..\recapis\nf-recapis-addwordstowordlist.md) | Adds one or more words to the word list. |
| [AdviseInkChange function](..\recapis\nf-recapis-adviseinkchange.md) | Stops the recognizer from processing ink because a stroke has been added or deleted. |
| [CloneContext function](..\recapis\nf-recapis-clonecontext.md) | Creates a recognizer context that contains the same settings as the original. The new recognizer context does not include the ink or recognition results of the original. |
| [CreateContext function](..\recapis\nf-recapis-createcontext.md) | Creates a recognizer context. |
| [CreateRecognizer function](..\recapis\nf-recapis-createrecognizer.md) | Creates a recognizer. |
| [DestroyAlternate function](..\recapis\nf-recapis-destroyalternate.md) | This function is obsolete and need not be implemented by custom application recognizers. |
| [DestroyContext function](..\recapis\nf-recapis-destroycontext.md) | Destroys a recognizer context. |
| [DestroyRecognizer function](..\recapis\nf-recapis-destroyrecognizer.md) | Destroys a recognizer. |
| [DestroyWordList function](..\recapis\nf-recapis-destroywordlist.md) | Destroys the current word list. |
| [EndInkInput function](..\recapis\nf-recapis-endinkinput.md) | Indicates that no more ink will be added to the context.You cannot add strokes to the context after calling this function. |
| [GetAllRecognizers function](..\recapis\nf-recapis-getallrecognizers.md) | Gets all recognizers. |
| [GetBestResultString function](..\recapis\nf-recapis-getbestresultstring.md) | Retrieves the best result string. |
| [GetContextPreferenceFlags function](..\recapis\nf-recapis-getcontextpreferenceflags.md) | Gets the context preference flags. |
| [GetContextPropertyList function](..\recapis\nf-recapis-getcontextpropertylist.md) | Retrieves a list of properties the recognizer supports. |
| [GetContextPropertyValue function](..\recapis\nf-recapis-getcontextpropertyvalue.md) | Returns a specified property value from the recognizer context. |
| [GetEnabledUnicodeRanges function](..\recapis\nf-recapis-getenabledunicoderanges.md) | Retrieves a list of Unicode point ranges enabled on the context. If you do not call the SetEnabledUnicodeRanges function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges. |
| [GetGuide function](..\recapis\nf-recapis-getguide.md) | Retrieves the guide used for boxed, lined, or freeform input. |
| [GetLatticePtr function](..\recapis\nf-recapis-getlatticeptr.md) | Retrieves a pointer to the lattice for the current results. |
| [GetLeftSeparator function](..\recapis\nf-recapis-getleftseparator.md) | Gets the left separator for the recognizer context. |
| [GetPreferredPacketDescription function](..\recapis\nf-recapis-getpreferredpacketdescription.md) | Retrieves a packet description that contains the packet properties the recognizer uses. |
| [GetRecoAttributes function](..\recapis\nf-recapis-getrecoattributes.md) | Retrieves the attributes of the recognizer. |
| [GetResultPropertyList function](..\recapis\nf-recapis-getresultpropertylist.md) | Retrieves a list of properties the recognizer can return for a result range. |
| [GetRightSeparator function](..\recapis\nf-recapis-getrightseparator.md) | Gets the right separator for the recognizer context. |
| [GetUnicodeRanges function](..\recapis\nf-recapis-getunicoderanges.md) | Returns the ranges of Unicode points that the recognizer supports. |
| [IsStringSupported function](..\recapis\nf-recapis-isstringsupported.md) | Returns a value that indicates whether a word, date, time, number, or other text that is passed in is contained in the dictionary.The results of this test depend on the factoid setting. |
| [LoadCachedAttributes function](..\recapis\nf-recapis-loadcachedattributes.md) | Loads the cached attributes of a recognizer. |
| [MakeWordList function](..\recapis\nf-recapis-makewordlist.md) | Creates a word list. |
| [Process function](..\recapis\nf-recapis-process.md) | Performs ink recognition synchronously. |
| [ResetContext function](..\recapis\nf-recapis-resetcontext.md) | Deletes the current ink and recognition results from the context.The current settings of the recognizer context are preserved. |
| [SetCACMode function](..\recapis\nf-recapis-setcacmode.md) | Specifies character Autocomplete mode for character or word recognition.You cannot turn off character Autocomplete after it is set. |
| [SetContextPropertyValue function](..\recapis\nf-recapis-setcontextpropertyvalue.md) | Adds a property to the recognizer context.If a property already exists, its value is modified. |
| [SetEnabledUnicodeRanges function](..\recapis\nf-recapis-setenabledunicoderanges.md) | Enables one or more Unicode point ranges on the context. |
| [SetFactoid function](..\recapis\nf-recapis-setfactoid.md) | Specifies the factoid a recognizer uses to constrain its search for the result.You specify a factoid if an input field is of a known type, such as if the input field contains a date. |
| [SetFlags function](..\recapis\nf-recapis-setflags.md) | Specifies how the recognizer interprets the ink and determines the result string.Call this function before processing the ink for the first time. Therefore, call the SetFlags function before calling the Process function. |
| [SetGuide function](..\recapis\nf-recapis-setguide.md) | Sets the recognition guide to use for boxed or lined input. You must call this function before you add strokes to the context. |
| [SetTextContext function](..\recapis\nf-recapis-settextcontext.md) | Provides the text strings that come before and after the text contained in the recognizer context.You call this function before processing the ink for the first time. Therefore, call the SetTextContext function before calling the Process function. |
| [SetWordList function](..\recapis\nf-recapis-setwordlist.md) | Sets the word list for the current recognizer context to recognize. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [FLICK_DATA structure](..\tabflicks\ns-tabflicks-flick_data.md) | Contains information about a pen flick. |
| [FLICK_POINT structure](..\tabflicks\ns-tabflicks-flick_point.md) | Provides information about a pen flick. |
| [IEC_GESTUREINFO structure](..\inked\ns-inked-iec_gestureinfo.md) | Contains information about a specific gesture. |
| [IEC_RECOGNITIONRESULTINFO structure](..\inked\ns-inked-iec_recognitionresultinfo.md) | Contains information about an IInkRecognitionResult Interface object. |
| [IEC_STROKEINFO structure](..\inked\ns-inked-iec_strokeinfo.md) | Contains information about a Stroke event. |
| [StylusInfo structure](..\rtscom\ns-rtscom-stylusinfo.md) | Provides information about the stylus. |
| [_InkRecoGuide structure](..\msinkaut\ns-msinkaut-_inkrecoguide.md) | Deprecated. Represents information about the recognition guide. Use the WritingBox Property, DrawnBox Property, Rows Property, Columns Property, and Midline Property [InkRecognizerGuide Class] properties instead. |
| [_PACKET_DESCRIPTION structure](..\tpcshrd\ns-tpcshrd-_packet_description.md) | Describes the content of the packet for a particular tablet recognizer context.Do not use this structure to access the data contained in a packet. This structure describes the content of the packet. |
| [_PACKET_PROPERTY structure](..\tpcshrd\ns-tpcshrd-_packet_property.md) | Describes a packet property that is reported by the tablet driver. |
| [_PROPERTY_METRICS structure](..\tpcshrd\ns-tpcshrd-_property_metrics.md) | Defines the range and resolution of a packet property. |
| [tagCHARACTER_RANGE structure](..\rectypes\ns-rectypes-tagcharacter_range.md) | Specifies a range of Unicode points (characters). |
| [tagINKMETRIC structure](..\msinkaut\ns-msinkaut-taginkmetric.md) | Specifies display properties for a text ink object (tInk). |
| [tagLATTICE_METRICS structure](..\rectypes\ns-rectypes-taglattice_metrics.md) | Describes the baseline and the midline height. |
| [tagLINE_SEGMENT structure](..\rectypes\ns-rectypes-tagline_segment.md) | Describes the start and end points of a line recognition segment, such as the baseline or midline. |
| [tagRECO_ATTRS structure](..\rectypes\ns-rectypes-tagreco_attrs.md) | Retrieves the attributes of a recognizer or specifies which attributes to use when you search for an installed recognizer. |
| [tagRECO_GUIDE structure](..\rectypes\ns-rectypes-tagreco_guide.md) | Defines the boundaries of the ink to the recognizer. |
| [tagRECO_LATTICE structure](..\rectypes\ns-rectypes-tagreco_lattice.md) | Serves as the entry point into a lattice. |
| [tagRECO_LATTICE_COLUMN structure](..\rectypes\ns-rectypes-tagreco_lattice_column.md) | Represents a column in the lattice. |
| [tagRECO_LATTICE_ELEMENT structure](..\rectypes\ns-rectypes-tagreco_lattice_element.md) | Corresponds to one word or one East Asian character, typically; however, an element may also correspond to a gesture, a shape, or some other code. |
| [tagRECO_LATTICE_PROPERTIES structure](..\rectypes\ns-rectypes-tagreco_lattice_properties.md) | Contains an array of pointers to property structures. |
| [tagRECO_LATTICE_PROPERTY structure](..\rectypes\ns-rectypes-tagreco_lattice_property.md) | Contains a property used in the lattice. |
| [tagRECO_RANGE structure](..\rectypes\ns-rectypes-tagreco_range.md) | The structure is obsolete. |
| [tagSTROKE_RANGE structure](..\tpcshrd\ns-tpcshrd-tagstroke_range.md) | Specifies a range of strokes in the InkDisp object. |
| [tagSYSTEM_EVENT_DATA structure](..\tpcshrd\ns-tpcshrd-tagsystem_event_data.md) | Contains information about a tablet system event. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [AppearanceConstants enumeration](..\inked\ne-inked-appearanceconstants.md) | Specifies how an InkEdit control appears on the screen. |
| [BorderStyleConstants enumeration](..\inked\ne-inked-borderstyleconstants.md) | Specifies how the borders of an InkEdit control appear on the screen. |
| [FLICKACTION_COMMANDCODE enumeration](..\tabflicks\ne-tabflicks-flickaction_commandcode.md) | Defines the possible flick actions that can be assigned to a pen flick. |
| [FLICKDIRECTION enumeration](..\tabflicks\ne-tabflicks-flickdirection.md) | Defines the directions in which a pen flick has occurred. |
| [FLICKMODE enumeration](..\tabflicks\ne-tabflicks-flickmode.md) | Describes where Flick gestures are enabled. |
| [InkApplicationGesture enumeration](..\msinkaut\ne-msinkaut-inkapplicationgesture.md) | Defines values that set the interest in a set of application-specific gesture. |
| [InkBoundingBoxMode enumeration](..\msinkaut\ne-msinkaut-inkboundingboxmode.md) | Specifies which characteristics of a stroke, such as drawing attributes, are used to calculate the bounding box of the ink.The bounding box is the smallest rectangle that includes all points in the InkDisp object. |
| [InkClipboardFormats enumeration](..\msinkaut\ne-msinkaut-inkclipboardformats.md) | Specifies the format of ink that is stored on the Clipboard. |
| [InkClipboardModes enumeration](..\msinkaut\ne-msinkaut-inkclipboardmodes.md) | Specifies the copy options of the Clipboard. |
| [InkCollectionMode enumeration](..\msinkaut\ne-msinkaut-inkcollectionmode.md) | Defines values that determine whether ink, gestures, or ink and gestures are recognized as the user writes. |
| [InkCollectorEventInterest enumeration](..\msinkaut\ne-msinkaut-inkcollectoreventinterest.md) | Defines values that are used to specify whether an event occurred on an ink collector and, if so, which event fired. |
| [InkCursorButtonState enumeration](..\msinkaut\ne-msinkaut-inkcursorbuttonstate.md) | Defines values that specify the state of a cursor button. |
| [InkDisplayMode enumeration](..\inked\ne-inked-inkdisplaymode.md) | Specifies how a selection appears on the control. |
| [InkEditStatus enumeration](..\inked\ne-inked-inkeditstatus.md) | Specifies whether the InkEdit control is idle, collecting ink, or recognizing ink. |
| [InkExtractFlags enumeration](..\msinkaut\ne-msinkaut-inkextractflags.md) | Determines how a stroke is removed from an InkDisp object. |
| [InkInsertMode enumeration](..\inked\ne-inked-inkinsertmode.md) | Specifies how ink is inserted onto the InkEdit control. |
| [InkMode enumeration](..\inked\ne-inked-inkmode.md) | Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected. |
| [InkMouseButton enumeration](..\msinkaut\ne-msinkaut-inkmousebutton.md) | Specifies which mouse button was pressed. |
| [InkMousePointer enumeration](..\msinkaut\ne-msinkaut-inkmousepointer.md) | Specifies the type of mouse pointer to appear. |
| [InkOverlayAttachMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayattachmode.md) | Specifies where to attach the new InkOverlay object, behind or in front of the active layer. |
| [InkOverlayEditingMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayeditingmode.md) | Specifies the behavior mode of the InkOverlay object and the InkPicture control. |
| [InkOverlayEraserMode enumeration](..\msinkaut\ne-msinkaut-inkoverlayerasermode.md) | Specifies the way in which ink is erased from the InkOverlay object and the InkPicture control.This mode is used when the InkOverlayEditingMode is set to Delete. |
| [InkPenTip enumeration](..\msinkaut\ne-msinkaut-inkpentip.md) | Specifies the pen-tip shape. |
| [InkPersistenceCompressionMode enumeration](..\msinkaut\ne-msinkaut-inkpersistencecompressionmode.md) | Defines values for the compression modes that are used to save the InkDisp object to a serialized format. |
| [InkPersistenceFormat enumeration](..\msinkaut\ne-msinkaut-inkpersistenceformat.md) | Specifies how ink is persisted. |
| [InkPictureSizeMode enumeration](..\msinkaut\ne-msinkaut-inkpicturesizemode.md) | Specifies how the picture behaves inside the InkPicture control. |
| [InkRasterOperation enumeration](..\msinkaut\ne-msinkaut-inkrasteroperation.md) | Defines values for performing raster operations on drawn ink. |
| [InkRecognitionAlternatesSelection enumeration](..\msinkaut\ne-msinkaut-inkrecognitionalternatesselection.md) | Not implemented. |
| [InkRecognitionConfidence enumeration](..\msinkaut\ne-msinkaut-inkrecognitionconfidence.md) | Indicates the level of confidence that the recognizer has in the recognition result. |
| [InkRecognitionModes enumeration](..\msinkaut\ne-msinkaut-inkrecognitionmodes.md) | Specifies how the recognizer interprets the ink and determines the result string. |
| [InkRecognitionStatus enumeration](..\msinkaut\ne-msinkaut-inkrecognitionstatus.md) | Specifies whether an error occurred during recognition and, if so, which error occurred. |
| [InkRecognizerCapabilities enumeration](..\msinkaut\ne-msinkaut-inkrecognizercapabilities.md) | Specifies the attributes of a recognizer. You also use this enumeration to determine which attributes to use when you search for an installed recognizer. |
| [InkRecognizerCharacterAutoCompletionMode enumeration](..\msinkaut\ne-msinkaut-inkrecognizercharacterautocompletionmode.md) | Specifies types of character input modes. |
| [InkShiftKeyModifierFlags enumeration](..\msinkaut\ne-msinkaut-inkshiftkeymodifierflags.md) | Specifies which modifier key was pressed. |
| [InkSystemGesture enumeration](..\msinkaut\ne-msinkaut-inksystemgesture.md) | Specifies the interest in a set of operating system-specific gestures. |
| [ItemSelectionConstants enumeration](..\msinkaut\ne-msinkaut-itemselectionconstants.md) | Specifies whether the first element or all elements within a group of points or packet values are used. |
| [KEYMODIFIER enumeration](..\tabflicks\ne-tabflicks-keymodifier.md) | Determines which, if any, modifier keys were pressed when the flick gesture occurred. |
| [MouseButton enumeration](..\inked\ne-inked-mousebutton.md) | Specifies which mouse button was pressed. |
| [RealTimeStylusDataInterest enumeration](..\rtscom\ne-rtscom-realtimestylusdatainterest.md) | Defines the values used by plug-ins to specify which event notifications the plug-ins receive. |
| [RealTimeStylusLockType enumeration](..\rtscom\ne-rtscom-realtimestyluslocktype.md) | Specifies the locks within the RealTimeStylus Class object that protect the RealTimeStylus Class object's members and properties from modification. |
| [SCROLLDIRECTION enumeration](..\tabflicks\ne-tabflicks-scrolldirection.md) | Defines the direction of the scrolling command for a pen flick. |
| [ScrollBarsConstants enumeration](..\inked\ne-inked-scrollbarsconstants.md) | Specifies how the scroll bars of an InkEdit control appear on the screen. |
| [SelAlignmentConstants enumeration](..\inked\ne-inked-selalignmentconstants.md) | Specifies the alignment of the paragraph relative to the margins of the InkEdit control. |
| [SelectionHitResult enumeration](..\msinkaut\ne-msinkaut-selectionhitresult.md) | Specifies which part of a selection, if any, was hit during a hit test. |
| [StylusQueue enumeration](..\rtscom\ne-rtscom-stylusqueue.md) | Specifies the queue to which stylus data is added. |
| [TabletHardwareCapabilities enumeration](..\msinkaut\ne-msinkaut-tablethardwarecapabilities.md) | Specifies the hardware capabilities of the Tablet PC. |
| [TabletPropertyMetricUnit enumeration](..\msinkaut\ne-msinkaut-tabletpropertymetricunit.md) | Indicates the unit of measurement of a property. |
| [_PROPERTY_UNITS enumeration](..\tpcshrd\ne-tpcshrd-_property_units.md) | Defines constant values for the unit of measurement of a property. |
| [__MIDL___MIDL_itf_micaut_0000_0000_0001 enumeration](..\micaut\ne-micaut-__midl___midl_itf_micaut_0000_0000_0001.md) | Specifies the user interface (UI) elements of a math input control (MIC). |
| [__MIDL___MIDL_itf_micaut_0000_0000_0002 enumeration](..\micaut\ne-micaut-__midl___midl_itf_micaut_0000_0000_0002.md) | Specifies the button states of a math input control (MIC). |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0001 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0001.md) | Specifies the interaction modes that can be chosen by the user for the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0002 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0002.md) | Specifies the In-Place state values of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0003 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0003.md) | Specifies the values that represent the default input areas of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0004 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0004.md) | Specifies the correction modes of the Tablet PC Input Panel. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0005 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0005.md) | Specifies the direction, relative to Input Panel, that the post insertion correction comb displays. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0006 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0006.md) | Specifies the preferred direction of the In-Place Input Panel relative to the text entry field. |
| [__MIDL___MIDL_itf_peninputpanel_0000_0000_0007 enumeration](..\peninputpanel\ne-peninputpanel-__midl___midl_itf_peninputpanel_0000_0000_0007.md) | The events on the ITextInputPanel Interface that you can set attention for. |
| [enumALT_BREAKS enumeration](..\rectypes\ne-rectypes-enumalt_breaks.md) | Specifiers how to create alternates from a best result string. |
| [enumCONFIDENCE_LEVEL enumeration](..\rectypes\ne-rectypes-enumconfidence_level.md) | Indicates the level of confidence the recognizer has in the recognition result. |
| [enumLINE_METRICS enumeration](..\rectypes\ne-rectypes-enumline_metrics.md) | Represents the lines found in a recognition segment. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDynamicRenderer interface](..\rtscom\nn-rtscom-idynamicrenderer.md) | Displays the tablet pen data in real-time as that data is being handled by the RealTimeStylus Class object. |
| [IGestureRecognizer interface](..\rtscom\nn-rtscom-igesturerecognizer.md) | Reacts to events by recognizing gestures and adding gesture data to the input queue. |
| [IHandwrittenTextInsertion interface](..\peninputpanel\nn-peninputpanel-ihandwrittentextinsertion.md) | Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store. |
| [IInkCursor interface](..\msinkaut\nn-msinkaut-iinkcursor.md) | Represents general information about the tablet cursor. |
| [IInkCursorButton interface](..\msinkaut\nn-msinkaut-iinkcursorbutton.md) | Represents general information about a button on a tablet pointing and selecting device. |
| [IInkCursorButtons interface](..\msinkaut\nn-msinkaut-iinkcursorbuttons.md) | Represents a collection of IInkCursorButton objects for an IInkCursor interface. |
| [IInkCursors interface](..\msinkaut\nn-msinkaut-iinkcursors.md) | Represents a collection of IInkCursor objects. |
| [IInkCustomStrokes interface](..\msinkaut\nn-msinkaut-iinkcustomstrokes.md) | Contains a collection of user-defined InkStrokes collections. |
| [IInkDivisionResult interface](..\msinkaut15\nn-msinkaut15-iinkdivisionresult.md) | Represents the layout analysis of the collection of strokes contained by the InkDivider object. |
| [IInkDivisionUnit interface](..\msinkaut15\nn-msinkaut15-iinkdivisionunit.md) | Represents a single structural element within an IInkDivisionResult object. |
| [IInkDivisionUnits interface](..\msinkaut15\nn-msinkaut15-iinkdivisionunits.md) | Contains a collection of IInkDivisionUnit objects that are contained in an IInkDivisionResult object. |
| [IInkEdit interface](..\inked\nn-inked-iinkedit.md) | "." |
| [IInkExtendedProperties interface](..\msinkaut\nn-msinkaut-iinkextendedproperties.md) | Represents a collection of IInkExtendedProperty objects that contain application-defined data. |
| [IInkExtendedProperty interface](..\msinkaut\nn-msinkaut-iinkextendedproperty.md) | Represents the ability to add your own data to a variety of objects within the Tablet PC object model. |
| [IInkGesture interface](..\msinkaut\nn-msinkaut-iinkgesture.md) | Represents the ability to query particular properties of a gesture returned from a gesture recognition. |
| [IInkLineInfo interface](..\msinkaut\nn-msinkaut-iinklineinfo.md) | The IInkLineInfo interface provides access to the display properties and recognition result list of a text ink object (tInk). |
| [IInkRecognitionAlternate interface](..\msinkaut\nn-msinkaut-iinkrecognitionalternate.md) | Represents the possible word matches for segments of ink that are compared to a recognizers dictionary. |
| [IInkRecognitionAlternates interface](..\msinkaut\nn-msinkaut-iinkrecognitionalternates.md) | Contains the IInkRecognitionAlternate objects that represent possible word matches for segments of ink. |
| [IInkRecognitionResult interface](..\msinkaut\nn-msinkaut-iinkrecognitionresult.md) | Represents the result of the recognition. The results of recognizing handwritten ink are returned in an IInkRecognitionResult object. |
| [IInkRecognizer interface](..\msinkaut\nn-msinkaut-iinkrecognizer.md) | Represents the ability to process ink, or handwriting, and translate the stroke into text or gesture. The recognizer creates an InkRecognizerContext object, which is used to perform the actual handwriting recognition. |
| [IInkRecognizer2 interface](..\msinkaut\nn-msinkaut-iinkrecognizer2.md) | Adds members to the IInkWordList2 Interface. |
| [IInkRecognizerContext2 interface](..\msinkaut\nn-msinkaut-iinkrecognizercontext2.md) | Adds members to the InkRecognizerContext Class. |
| [IInkStrokeDisp interface](..\msinkaut\nn-msinkaut-iinkstrokedisp.md) | Represents a single ink stroke. |
| [IInkTablet interface](..\msinkaut\nn-msinkaut-iinktablet.md) | Represents the digitizer device of Tablet PC that receives tablet device messages or events. |
| [IInkTablet2 interface](..\msinkaut\nn-msinkaut-iinktablet2.md) | Extends the IInkTablet interface. |
| [IInkWordList2 interface](..\msinkaut\nn-msinkaut-iinkwordlist2.md) | Adds members to the InkWordList Class. |
| [IMathInputControl interface](..\micaut\nn-micaut-imathinputcontrol.md) | Exposes methods that turn ink input into interpreted math output. |
| [IRealTimeStylus interface](..\rtscom\nn-rtscom-irealtimestylus.md) | Handles the stylus packet data from a digitizer in real time. |
| [IRealTimeStylus2 interface](..\rtscom\nn-rtscom-irealtimestylus2.md) | Extends the IRealTimeStylus interface. |
| [IRealTimeStylus3 interface](..\rtscom\nn-rtscom-irealtimestylus3.md) | The IRealTimeStylus3 interface enables multitouch for the realtime stylus. |
| [IRealTimeStylusSynchronization interface](..\rtscom\nn-rtscom-irealtimestylussynchronization.md) | Synchronizes access to the RealTimeStylus Class object. |
| [IStrokeBuilder interface](..\rtscom\nn-rtscom-istrokebuilder.md) | Use interface to programmatically create strokes from packet data. |
| [IStylusPlugin interface](..\rtscom\nn-rtscom-istylusplugin.md) | Receives notifications of RealTimeStylus Class events to enable you to perform custom processing based on those events. |
| [ITextInputPanel interface](..\peninputpanel\nn-peninputpanel-itextinputpanel.md) | Provides control of appearance and behavior of the Tablet PC Input Panel. |
| [ITextInputPanelEventSink interface](..\peninputpanel\nn-peninputpanel-itextinputpaneleventsink.md) | Defines methods that handle the ITextInputPanel Interface events. |
| [ITextInputPanelRunInfo interface](..\peninputpanel\nn-peninputpanel-itextinputpanelruninfo.md) | Provides a method to determine if the Text Input Panel is currently running. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDynamicRenderer::Draw](..\rtscom\nf-rtscom-idynamicrenderer-draw.md) | Draws the cached data to the specified device context. |
| [IDynamicRenderer::Refresh](..\rtscom\nf-rtscom-idynamicrenderer-refresh.md) | Causes the DynamicRenderer Class object to redraw the ink data that is currently rendering. |
| [IDynamicRenderer::ReleaseCachedData](..\rtscom\nf-rtscom-idynamicrenderer-releasecacheddata.md) | Releases specified stroke data from the temporal data held by DynamicRenderer Class. |
| [IDynamicRenderer::get_ClipRectangle](..\rtscom\nf-rtscom-idynamicrenderer-get_cliprectangle.md) | Gets or sets the clipping rectangle for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_ClipRegion](..\rtscom\nf-rtscom-idynamicrenderer-get_clipregion.md) | Gets or sets the clipping region for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_DataCacheEnabled](..\rtscom\nf-rtscom-idynamicrenderer-get_datacacheenabled.md) | Gets or sets a value that indicates whether data caching is enabled for the DynamicRenderer Class object. |
| [IDynamicRenderer::get_DrawingAttributes](..\rtscom\nf-rtscom-idynamicrenderer-get_drawingattributes.md) | Gets or sets the DrawingAttributes object used by the DynamicRenderer Class object. |
| [IDynamicRenderer::get_Enabled](..\rtscom\nf-rtscom-idynamicrenderer-get_enabled.md) | Gets or sets a value that turns dynamic rendering on and off. |
| [IDynamicRenderer::get_HWND](..\rtscom\nf-rtscom-idynamicrenderer-get_hwnd.md) | Gets or sets the window handle, HWND, associated with the DynamicRenderer Class object. |
| [IDynamicRenderer::put_ClipRectangle](..\rtscom\nf-rtscom-idynamicrenderer-put_cliprectangle.md) | Gets or sets the clipping rectangle for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_ClipRegion](..\rtscom\nf-rtscom-idynamicrenderer-put_clipregion.md) | Gets or sets the clipping region for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_DataCacheEnabled](..\rtscom\nf-rtscom-idynamicrenderer-put_datacacheenabled.md) | Gets or sets a value that indicates whether data caching is enabled for the DynamicRenderer Class object. |
| [IDynamicRenderer::put_Enabled](..\rtscom\nf-rtscom-idynamicrenderer-put_enabled.md) | Gets or sets a value that turns dynamic rendering on and off. |
| [IDynamicRenderer::put_HWND](..\rtscom\nf-rtscom-idynamicrenderer-put_hwnd.md) | Gets or sets the window handle, HWND, associated with the DynamicRenderer Class object. |
| [IGestureRecognizer::EnableGestures](..\rtscom\nf-rtscom-igesturerecognizer-enablegestures.md) | Sets a value that indicates to which application gestures the GestureRecognizer Class object responds. |
| [IGestureRecognizer::Reset](..\rtscom\nf-rtscom-igesturerecognizer-reset.md) | Deletes past stroke information from the GestureRecognizer Class object. |
| [IGestureRecognizer::get_Enabled](..\rtscom\nf-rtscom-igesturerecognizer-get_enabled.md) | Gets or sets a value that indicates whether gesture recognition is enabled. |
| [IGestureRecognizer::get_MaxStrokeCount](..\rtscom\nf-rtscom-igesturerecognizer-get_maxstrokecount.md) | Gets or sets the maximum number of strokes allowed per gesture recognition. |
| [IGestureRecognizer::put_Enabled](..\rtscom\nf-rtscom-igesturerecognizer-put_enabled.md) | Gets or sets a value that indicates whether gesture recognition is enabled. |
| [IGestureRecognizer::put_MaxStrokeCount](..\rtscom\nf-rtscom-igesturerecognizer-put_maxstrokecount.md) | Gets or sets the maximum number of strokes allowed per gesture recognition. |
| [IHandwrittenTextInsertion::InsertInkRecognitionResult](..\peninputpanel\nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult.md) | Inserts recognition results. |
| [IHandwrittenTextInsertion::InsertRecognitionResultsArray](..\peninputpanel\nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray.md) | Insert recognition results array. |
| [IInkCollector::GetEventInterest](..\msinkaut\nf-msinkaut-iinkcollector-geteventinterest.md) | Retrieves the interest an object has in a particular event for the InkCollector class, InkOverlay class, or InkPicture class. |
| [IInkCollector::GetGestureStatus](..\msinkaut\nf-msinkaut-iinkcollector-getgesturestatus.md) | Indicates whether the InkCollector or InkOverlay object is interested in a particular application gesture. |
| [IInkCollector::GetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkcollector-getwindowinputrectangle.md) | Gets the window rectangle, in pixels, within which ink is drawn. |
| [IInkCollector::SetAllTabletsMode](..\msinkaut\nf-msinkaut-iinkcollector-setalltabletsmode.md) | Allows an ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from any tablet attached to the Tablet PC. |
| [IInkCollector::SetEventInterest](..\msinkaut\nf-msinkaut-iinkcollector-seteventinterest.md) | Modifies a value that indicates whether an object or control has interest in a specified event. |
| [IInkCollector::SetGestureStatus](..\msinkaut\nf-msinkaut-iinkcollector-setgesturestatus.md) | Modifies the interest of the object or control in a known gesture. |
| [IInkCollector::SetSingleTabletIntegratedMode](..\msinkaut\nf-msinkaut-iinkcollector-setsingletabletintegratedmode.md) | Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector. |
| [IInkCollector::SetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkcollector-setwindowinputrectangle.md) | Sets the window rectangle, in pixels, within which ink is drawn. |
| [IInkCollector::get_AutoRedraw](..\msinkaut\nf-msinkaut-iinkcollector-get_autoredraw.md) | Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated. |
| [IInkCollector::get_CollectingInk](..\msinkaut\nf-msinkaut-iinkcollector-get_collectingink.md) | Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). |
| [IInkCollector::get_CollectionMode](..\msinkaut\nf-msinkaut-iinkcollector-get_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. |
| [IInkCollector::get_Cursors](..\msinkaut\nf-msinkaut-iinkcollector-get_cursors.md) | Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device. |
| [IInkCollector::get_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkcollector-get_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkCollector::get_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkcollector-get_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkCollector::get_DynamicRendering](..\msinkaut\nf-msinkaut-iinkcollector-get_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkCollector::get_Enabled](..\msinkaut\nf-msinkaut-iinkcollector-get_enabled.md) | Gets or sets a value that specifies whether the InkCollector object collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkCollector::get_Ink](..\msinkaut\nf-msinkaut-iinkcollector-get_ink.md) | Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. |
| [IInkCollector::get_MarginX](..\msinkaut\nf-msinkaut-iinkcollector-get_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkCollector::get_MarginY](..\msinkaut\nf-msinkaut-iinkcollector-get_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkCollector::get_MouseIcon](..\msinkaut\nf-msinkaut-iinkcollector-get_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkCollector::get_MousePointer](..\msinkaut\nf-msinkaut-iinkcollector-get_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkCollector::get_Renderer](..\msinkaut\nf-msinkaut-iinkcollector-get_renderer.md) | Gets or sets the InkRenderer object that is used to draw ink. |
| [IInkCollector::get_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkcollector-get_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkCollector::get_Tablet](..\msinkaut\nf-msinkaut-iinkcollector-get_tablet.md) | Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. |
| [IInkCollector::get_hWnd](..\msinkaut\nf-msinkaut-iinkcollector-get_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkCollector::put_AutoRedraw](..\msinkaut\nf-msinkaut-iinkcollector-put_autoredraw.md) | Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated. |
| [IInkCollector::put_CollectionMode](..\msinkaut\nf-msinkaut-iinkcollector-put_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. |
| [IInkCollector::put_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkcollector-put_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkCollector::put_DynamicRendering](..\msinkaut\nf-msinkaut-iinkcollector-put_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkCollector::put_Enabled](..\msinkaut\nf-msinkaut-iinkcollector-put_enabled.md) | Gets or sets a value that specifies whether the InkCollector object collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkCollector::put_MarginX](..\msinkaut\nf-msinkaut-iinkcollector-put_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkCollector::put_MarginY](..\msinkaut\nf-msinkaut-iinkcollector-put_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkCollector::put_MousePointer](..\msinkaut\nf-msinkaut-iinkcollector-put_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkCollector::put_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkcollector-put_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkCollector::put_hWnd](..\msinkaut\nf-msinkaut-iinkcollector-put_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkCollector::putref_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkcollector-putref_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkCollector::putref_Ink](..\msinkaut\nf-msinkaut-iinkcollector-putref_ink.md) | Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. |
| [IInkCollector::putref_MouseIcon](..\msinkaut\nf-msinkaut-iinkcollector-putref_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkCollector::putref_Renderer](..\msinkaut\nf-msinkaut-iinkcollector-putref_renderer.md) | Gets or sets the InkRenderer object that is used to draw ink. |
| [IInkCursor::get_Buttons](..\msinkaut\nf-msinkaut-iinkcursor-get_buttons.md) | Gets the IInkCursorButtons collection that is available on an IInkCursor. |
| [IInkCursor::get_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkcursor-get_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkCursor::get_Id](..\msinkaut\nf-msinkaut-iinkcursor-get_id.md) | Gets the identifier of an object. |
| [IInkCursor::get_Inverted](..\msinkaut\nf-msinkaut-iinkcursor-get_inverted.md) | Gets a value that indicates whether the cursor is the inverted end of the pen. |
| [IInkCursor::get_Name](..\msinkaut\nf-msinkaut-iinkcursor-get_name.md) | Gets the name of the object. |
| [IInkCursor::get_Tablet](..\msinkaut\nf-msinkaut-iinkcursor-get_tablet.md) | Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. |
| [IInkCursor::putref_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkcursor-putref_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkCursorButton::get_Id](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_id.md) | Gets the identifier of an object. |
| [IInkCursorButton::get_Name](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_name.md) | Gets the name of the object. |
| [IInkCursorButton::get_State](..\msinkaut\nf-msinkaut-iinkcursorbutton-get_state.md) | Gets the state of a cursor button, such as whether the button is unavailable, up, or down. |
| [IInkCursorButtons::Item](..\msinkaut\nf-msinkaut-iinkcursorbuttons-item.md) | Retrieves the IInkCursorButton object at the specified index or string identifier within the IInkCursorButtons collection. |
| [IInkCursorButtons::get_Count](..\msinkaut\nf-msinkaut-iinkcursorbuttons-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkCursors::Item](..\msinkaut\nf-msinkaut-iinkcursors-item.md) | Returns the IInkCursor object at the specified index within the IInkCursors collection. |
| [IInkCursors::get_Count](..\msinkaut\nf-msinkaut-iinkcursors-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkCustomStrokes::Add](..\msinkaut\nf-msinkaut-iinkcustomstrokes-add.md) | Adds an InkStrokes collection to an IInkCustomStrokes collection. |
| [IInkCustomStrokes::Clear](..\msinkaut\nf-msinkaut-iinkcustomstrokes-clear.md) | Clears all InkStrokes collections from the IInkCustomStrokes collection. |
| [IInkCustomStrokes::Item](..\msinkaut\nf-msinkaut-iinkcustomstrokes-item.md) | Retrieves the InkStrokes Collection at the location specified within the IInkCustomStrokes Interface. |
| [IInkCustomStrokes::Remove](..\msinkaut\nf-msinkaut-iinkcustomstrokes-remove.md) | Removes the InkStrokes collection from the IInkCustomStrokes collection. |
| [IInkCustomStrokes::get_Count](..\msinkaut\nf-msinkaut-iinkcustomstrokes-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkDisp::AddStrokesAtRectangle](..\msinkaut\nf-msinkaut-iinkdisp-addstrokesatrectangle.md) | Adds a specified Strokes collection into this InkDisp object at a specified rectangle. |
| [IInkDisp::CanPaste](..\msinkaut\nf-msinkaut-iinkdisp-canpaste.md) | Indicates whether the IDataObject can be converted to an InkDisp object. |
| [IInkDisp::Clip](..\msinkaut\nf-msinkaut-iinkdisp-clip.md) | Removes portions of an IInkStrokeDisp object or InkStrokes collection that are outside a rectangle. |
| [IInkDisp::ClipboardCopyWithRectangle](..\msinkaut\nf-msinkaut-iinkdisp-clipboardcopywithrectangle.md) | Copies the IInkStrokeDisp objects that are contained within the known rectangle to the Clipboard. |
| [IInkDisp::ClipboardCopy](..\msinkaut\nf-msinkaut-iinkdisp-clipboardcopy.md) | Copies the InkStrokes collection to the Clipboard. |
| [IInkDisp::ClipboardPaste](..\msinkaut\nf-msinkaut-iinkdisp-clipboardpaste.md) | Copies the IDataObject from the Clipboard to the InkDisp object. |
| [IInkDisp::Clone](..\msinkaut\nf-msinkaut-iinkdisp-clone.md) | Creates a duplicate InkDisp object. |
| [IInkDisp::CreateStroke](..\msinkaut\nf-msinkaut-iinkdisp-createstroke.md) | Creates an IInkStrokeDisp object from an array of packet data input values. |
| [IInkDisp::CreateStrokes](..\msinkaut\nf-msinkaut-iinkdisp-createstrokes.md) | Creates a new InkStrokes collection from existing IInkStrokeDisp objects. |
| [IInkDisp::DeleteStroke](..\msinkaut\nf-msinkaut-iinkdisp-deletestroke.md) | Deletes a IInkStrokeDisp object from the InkDisp object. |
| [IInkDisp::DeleteStrokes](..\msinkaut\nf-msinkaut-iinkdisp-deletestrokes.md) | Deletes an InkStrokes collection from the Strokes collection of the InkDisp object. |
| [IInkDisp::ExtractStrokes](..\msinkaut\nf-msinkaut-iinkdisp-extractstrokes.md) | Specifies the strokes to extract from an InkDisp Class and cut or copy into a new InkDisp Class, by using the known collection of strokes to determine which strokes to extract. |
| [IInkDisp::ExtractWithRectangle](..\msinkaut\nf-msinkaut-iinkdisp-extractwithrectangle.md) | Cuts or copies strokes from an existing InkDisp object and pastes them into a new InkDisp object, by using the known rectangle to determine which strokes to extract. |
| [IInkDisp::GetBoundingBox](..\msinkaut\nf-msinkaut-iinkdisp-getboundingbox.md) | Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection. |
| [IInkDisp::HitTestCircle](..\msinkaut\nf-msinkaut-iinkdisp-hittestcircle.md) | Retrieves the InkStrokes collection that are either completely inside or intersected by a known circle. |
| [IInkDisp::HitTestWithLasso](..\msinkaut\nf-msinkaut-iinkdisp-hittestwithlasso.md) | Retrieves the strokes within a polyline selection area. |
| [IInkDisp::HitTestWithRectangle](..\msinkaut\nf-msinkaut-iinkdisp-hittestwithrectangle.md) | Retrieves the strokes that are contained within a specified rectangle. |
| [IInkDisp::Load](..\msinkaut\nf-msinkaut-iinkdisp-load.md) | Populates a new InkDisp object with known binary data. |
| [IInkDisp::NearestPoint](..\msinkaut\nf-msinkaut-iinkdisp-nearestpoint.md) | Retrieves the IInkStrokeDisp within the InkDisp object that is nearest to a known point, optionally providing the index of the nearest point and the distance to the stroke from the specified point. |
| [IInkDisp::Save](..\msinkaut\nf-msinkaut-iinkdisp-save.md) | Converts the ink to the specified InkPersistenceFormat, saves the ink by using the specified InkPersistenceCompressionMode, and returns the binary data in an array of bytes. |
| [IInkDisp::get_CustomStrokes](..\msinkaut\nf-msinkaut-iinkdisp-get_customstrokes.md) | Gets the collection of custom strokes to be persisted with the ink. |
| [IInkDisp::get_Dirty](..\msinkaut\nf-msinkaut-iinkdisp-get_dirty.md) | Gets or sets the value that specifies whether the strokes of an InkDisp Class object have been modified since the last time the ink was saved. |
| [IInkDisp::get_ExtendedProperties](..\msinkaut\nf-msinkaut-iinkdisp-get_extendedproperties.md) | Gets the collection of application-defined data that are stored in an object. |
| [IInkDisp::get_Strokes](..\msinkaut\nf-msinkaut-iinkdisp-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkDisp::put_Dirty](..\msinkaut\nf-msinkaut-iinkdisp-put_dirty.md) | Gets or sets the value that specifies whether the strokes of an InkDisp Class object have been modified since the last time the ink was saved. |
| [IInkDivisionResult::ResultByType](..\msinkaut15\nf-msinkaut15-iinkdivisionresult-resultbytype.md) | Gets the requested structural units of the analysis results for an IInkDivisionUnits collection. |
| [IInkDivisionResult::get_Strokes](..\msinkaut15\nf-msinkaut15-iinkdivisionresult-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkDivisionUnit::get_DivisionType](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_divisiontype.md) | Gets the type of structural unit the IInkDivisionUnit object represents within the analysis results. |
| [IInkDivisionUnit::get_RotationTransform](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_rotationtransform.md) | Gets the transformation matrix that the IInkDivisionUnit object uses to rotate the strokes to horizontal. |
| [IInkDivisionUnit::get_Strokes](..\msinkaut15\nf-msinkaut15-iinkdivisionunit-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkDivisionUnits::Item](..\msinkaut15\nf-msinkaut15-iinkdivisionunits-item.md) | Retrieves the IInkDivisionUnit object at the specified index within the IInkDivisionUnits collection. |
| [IInkDivisionUnits::get_Count](..\msinkaut15\nf-msinkaut15-iinkdivisionunits-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkDrawingAttributes::Clone](..\msinkaut\nf-msinkaut-iinkdrawingattributes-clone.md) | Creates a duplicate InkDrawingAttributes object. |
| [IInkDrawingAttributes::get_AntiAliased](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_antialiased.md) | Gets or sets the value that indicates whether a stroke is antialiased. |
| [IInkDrawingAttributes::get_Color](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_color.md) | Gets or sets the color of the ink that is drawn with this InkDrawingAttributes object. |
| [IInkDrawingAttributes::get_ExtendedProperties](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_extendedproperties.md) | Gets the collection of application-defined data that are stored in an object. |
| [IInkDrawingAttributes::get_FitToCurve](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_fittocurve.md) | Gets or sets the value that specifies whether Bezier smoothing is used to render ink. |
| [IInkDrawingAttributes::get_Height](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_height.md) | Gets or sets the height of the pen when drawing ink with the InkDrawingAttributes object. |
| [IInkDrawingAttributes::get_IgnorePressure](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_ignorepressure.md) | Gets or sets the value that specifies whether drawn ink automatically gets wider with increased pressure of the pen tip on the tablet surface. |
| [IInkDrawingAttributes::get_PenTip](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_pentip.md) | Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this InkDrawingAttributes object. |
| [IInkDrawingAttributes::get_RasterOperation](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_rasteroperation.md) | Gets or sets a value that defines how the colors of the pen and background interact. |
| [IInkDrawingAttributes::get_Transparency](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_transparency.md) | Gets or sets a value that indicates the transparency value of ink. |
| [IInkDrawingAttributes::get_Width](..\msinkaut\nf-msinkaut-iinkdrawingattributes-get_width.md) | Gets or sets the y-axis dimension, or width, of the pen tip when drawing ink. |
| [IInkDrawingAttributes::put_AntiAliased](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_antialiased.md) | Gets or sets the value that indicates whether a stroke is antialiased. |
| [IInkDrawingAttributes::put_Color](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_color.md) | Gets or sets the color of the ink that is drawn with this InkDrawingAttributes object. |
| [IInkDrawingAttributes::put_FitToCurve](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_fittocurve.md) | Gets or sets the value that specifies whether Bezier smoothing is used to render ink. |
| [IInkDrawingAttributes::put_Height](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_height.md) | Gets or sets the height of the pen when drawing ink with the InkDrawingAttributes object. |
| [IInkDrawingAttributes::put_IgnorePressure](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_ignorepressure.md) | Gets or sets the value that specifies whether drawn ink automatically gets wider with increased pressure of the pen tip on the tablet surface. |
| [IInkDrawingAttributes::put_PenTip](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_pentip.md) | Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this InkDrawingAttributes object. |
| [IInkDrawingAttributes::put_RasterOperation](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_rasteroperation.md) | Gets or sets a value that defines how the colors of the pen and background interact. |
| [IInkDrawingAttributes::put_Transparency](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_transparency.md) | Gets or sets a value that indicates the transparency value of ink. |
| [IInkDrawingAttributes::put_Width](..\msinkaut\nf-msinkaut-iinkdrawingattributes-put_width.md) | Gets or sets the y-axis dimension, or width, of the pen tip when drawing ink. |
| [IInkEdit::GetGestureStatus](..\inked\nf-inked-iinkedit-getgesturestatus.md) | Indicates whether the InkEdit control is interested in a particular application gesture. |
| [IInkEdit::Recognize](..\inked\nf-inked-iinkedit-recognize.md) | Performs recognition on an InkStrokes collection and returns recognition results. |
| [IInkEdit::Refresh](..\inked\nf-inked-iinkedit-refresh.md) | Causes the InkEdit control to redraw. |
| [IInkEdit::SetGestureStatus](..\inked\nf-inked-iinkedit-setgesturestatus.md) | Modifies the interest of the InkEdit control in a known application gesture. |
| [IInkEdit::get_Appearance](..\inked\nf-inked-iinkedit-get_appearance.md) | Gets or sets a value that determines the appearance of the InkEdit control - whether it is flat (painted with no visual effects) or 3D (painted with three-dimensional effects). |
| [IInkEdit::get_BackColor](..\inked\nf-inked-iinkedit-get_backcolor.md) | Gets or sets the background color for the InkEdit control. |
| [IInkEdit::get_BorderStyle](..\inked\nf-inked-iinkedit-get_borderstyle.md) | Gets or sets a value that determines whether the InkEdit control has a border. |
| [IInkEdit::get_DisableNoScroll](..\inked\nf-inked-iinkedit-get_disablenoscroll.md) | Gets or sets a value that determines whether scroll bars in the InkEdit control are disabled. |
| [IInkEdit::get_DrawingAttributes](..\inked\nf-inked-iinkedit-get_drawingattributes.md) | Gets or sets the drawing attributes for ink that is yet to be drawn on the InkEdit control. |
| [IInkEdit::get_Enabled](..\inked\nf-inked-iinkedit-get_enabled.md) | Gets or sets a value that determines whether the InkEdit control can respond to user-generated events. |
| [IInkEdit::get_Factoid](..\inked\nf-inked-iinkedit-get_factoid.md) | Gets or sets the Factoid constant that a IInkRecognizer object uses to constrain its search for the recognition result. |
| [IInkEdit::get_Font](..\inked\nf-inked-iinkedit-get_font.md) | Gets or sets a Font object. |
| [IInkEdit::get_Hwnd](..\inked\nf-inked-iinkedit-get_hwnd.md) | Gets a handle to the InkEdit control. |
| [IInkEdit::get_InkInsertMode](..\inked\nf-inked-iinkedit-get_inkinsertmode.md) | Gets or sets a value that specifies how ink is inserted onto the InkEdit control, either as text or as ink. |
| [IInkEdit::get_InkMode](..\inked\nf-inked-iinkedit-get_inkmode.md) | Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected. |
| [IInkEdit::get_Locked](..\inked\nf-inked-iinkedit-get_locked.md) | Gets or sets a value indicating whether the contents of the InkEdit control can be edited. |
| [IInkEdit::get_MaxLength](..\inked\nf-inked-iinkedit-get_maxlength.md) | Gets or sets a value indicating whether there is a maximum number of characters an InkEdit control can hold and, if so, specifies the maximum number of characters. |
| [IInkEdit::get_MouseIcon](..\inked\nf-inked-iinkedit-get_mouseicon.md) | Gets or sets the custom mouse icon for the InkEdit control. |
| [IInkEdit::get_MousePointer](..\inked\nf-inked-iinkedit-get_mousepointer.md) | Gets or sets a value indicating the type of mouse pointer to be displayed. |
| [IInkEdit::get_MultiLine](..\inked\nf-inked-iinkedit-get_multiline.md) | Gets or sets a value indicating whether an InkEdit control can accept and display multiple lines of text. |
| [IInkEdit::get_RecognitionTimeout](..\inked\nf-inked-iinkedit-get_recognitiontimeout.md) | Gets or sets the length of time, in milliseconds, between the last IInkStrokeDisp object collected and the beginning of text recognition. |
| [IInkEdit::get_Recognizer](..\inked\nf-inked-iinkedit-get_recognizer.md) | Gets or sets the IInkRecognizer object to use for recognition. |
| [IInkEdit::get_ScrollBars](..\inked\nf-inked-iinkedit-get_scrollbars.md) | Gets or sets the type of scroll bars, if any, to display in the InkEdit control. |
| [IInkEdit::get_SelAlignment](..\inked\nf-inked-iinkedit-get_selalignment.md) | Gets or sets a value that controls the alignment of the paragraphs in an InkEdit control. |
| [IInkEdit::get_SelBold](..\inked\nf-inked-iinkedit-get_selbold.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is bold. |
| [IInkEdit::get_SelCharOffset](..\inked\nf-inked-iinkedit-get_selcharoffset.md) | Returns or sets a value that determines whether text in the InkEdit control appears on the baseline (normal), as a superscript above the baseline, or as a subscript below the baseline. |
| [IInkEdit::get_SelColor](..\inked\nf-inked-iinkedit-get_selcolor.md) | Gets or sets the text color of the current text selection or insertion point (run time only). |
| [IInkEdit::get_SelFontName](..\inked\nf-inked-iinkedit-get_selfontname.md) | Gets or sets the font name of the selected text within the InkEdit control (run time only). |
| [IInkEdit::get_SelFontSize](..\inked\nf-inked-iinkedit-get_selfontsize.md) | Gets or sets the font size of the selected text within the InkEdit control (run time only). |
| [IInkEdit::get_SelInksDisplayMode](..\inked\nf-inked-iinkedit-get_selinksdisplaymode.md) | Gets or sets a value that allows for toggling the appearance of the selection between ink and text. |
| [IInkEdit::get_SelInks](..\inked\nf-inked-iinkedit-get_selinks.md) | Gets or sets the array of embedded InkDisp objects (if displayed as ink) in the current selection. |
| [IInkEdit::get_SelItalic](..\inked\nf-inked-iinkedit-get_selitalic.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is italic (run time only). |
| [IInkEdit::get_SelLength](..\inked\nf-inked-iinkedit-get_sellength.md) | Gets or sets the number of characters that are selected in the InkEdit control (run time only). |
| [IInkEdit::get_SelRTF](..\inked\nf-inked-iinkedit-get_selrtf.md) | Gets or sets the currently selected Rich Text Format (RTF) formatted text in the InkEdit control (run time only). |
| [IInkEdit::get_SelStart](..\inked\nf-inked-iinkedit-get_selstart.md) | Gets or sets the starting point of the text that is selected in the InkEdit control (run time only). |
| [IInkEdit::get_SelText](..\inked\nf-inked-iinkedit-get_seltext.md) | Gets or sets the selected text within the InkEdit control (run time only). |
| [IInkEdit::get_SelUnderline](..\inked\nf-inked-iinkedit-get_selunderline.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is underlined (run time only). |
| [IInkEdit::get_Status](..\inked\nf-inked-iinkedit-get_status.md) | Gets a value that specifies whether the InkEdit control is idle, collecting ink, or recognizing ink. |
| [IInkEdit::get_TextRTF](..\inked\nf-inked-iinkedit-get_textrtf.md) | Gets or sets the text of the InkEdit control, including all RTF codes. |
| [IInkEdit::get_Text](..\inked\nf-inked-iinkedit-get_text.md) | Gets or sets the current text in the InkEdit control. |
| [IInkEdit::get_UseMouseForInput](..\inked\nf-inked-iinkedit-get_usemouseforinput.md) | Gets or sets a value that indicates whether the mouse can be used as an input device. |
| [IInkEdit::put_Appearance](..\inked\nf-inked-iinkedit-put_appearance.md) | Gets or sets a value that determines the appearance of the InkEdit control - whether it is flat (painted with no visual effects) or 3D (painted with three-dimensional effects). |
| [IInkEdit::put_BackColor](..\inked\nf-inked-iinkedit-put_backcolor.md) | Gets or sets the background color for the InkEdit control. |
| [IInkEdit::put_BorderStyle](..\inked\nf-inked-iinkedit-put_borderstyle.md) | Gets or sets a value that determines whether the InkEdit control has a border. |
| [IInkEdit::put_DisableNoScroll](..\inked\nf-inked-iinkedit-put_disablenoscroll.md) | Gets or sets a value that determines whether scroll bars in the InkEdit control are disabled. |
| [IInkEdit::put_Enabled](..\inked\nf-inked-iinkedit-put_enabled.md) | Gets or sets a value that determines whether the InkEdit control can respond to user-generated events. |
| [IInkEdit::put_Factoid](..\inked\nf-inked-iinkedit-put_factoid.md) | Gets or sets the Factoid constant that a IInkRecognizer object uses to constrain its search for the recognition result. |
| [IInkEdit::put_InkInsertMode](..\inked\nf-inked-iinkedit-put_inkinsertmode.md) | Gets or sets a value that specifies how ink is inserted onto the InkEdit control, either as text or as ink. |
| [IInkEdit::put_InkMode](..\inked\nf-inked-iinkedit-put_inkmode.md) | Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected. |
| [IInkEdit::put_Locked](..\inked\nf-inked-iinkedit-put_locked.md) | Gets or sets a value indicating whether the contents of the InkEdit control can be edited. |
| [IInkEdit::put_MaxLength](..\inked\nf-inked-iinkedit-put_maxlength.md) | Gets or sets a value indicating whether there is a maximum number of characters an InkEdit control can hold and, if so, specifies the maximum number of characters. |
| [IInkEdit::put_MouseIcon](..\inked\nf-inked-iinkedit-put_mouseicon.md) | Gets or sets the custom mouse icon for the InkEdit control. |
| [IInkEdit::put_MousePointer](..\inked\nf-inked-iinkedit-put_mousepointer.md) | Gets or sets a value indicating the type of mouse pointer to be displayed. |
| [IInkEdit::put_MultiLine](..\inked\nf-inked-iinkedit-put_multiline.md) | Gets or sets a value indicating whether an InkEdit control can accept and display multiple lines of text. |
| [IInkEdit::put_RecognitionTimeout](..\inked\nf-inked-iinkedit-put_recognitiontimeout.md) | Gets or sets the length of time, in milliseconds, between the last IInkStrokeDisp object collected and the beginning of text recognition. |
| [IInkEdit::put_ScrollBars](..\inked\nf-inked-iinkedit-put_scrollbars.md) | Gets or sets the type of scroll bars, if any, to display in the InkEdit control. |
| [IInkEdit::put_SelAlignment](..\inked\nf-inked-iinkedit-put_selalignment.md) | Gets or sets a value that controls the alignment of the paragraphs in an InkEdit control. |
| [IInkEdit::put_SelBold](..\inked\nf-inked-iinkedit-put_selbold.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is bold. |
| [IInkEdit::put_SelCharOffset](..\inked\nf-inked-iinkedit-put_selcharoffset.md) | Returns or sets a value that determines whether text in the InkEdit control appears on the baseline (normal), as a superscript above the baseline, or as a subscript below the baseline. |
| [IInkEdit::put_SelColor](..\inked\nf-inked-iinkedit-put_selcolor.md) | Gets or sets the text color of the current text selection or insertion point (run time only). |
| [IInkEdit::put_SelFontName](..\inked\nf-inked-iinkedit-put_selfontname.md) | Gets or sets the font name of the selected text within the InkEdit control (run time only). |
| [IInkEdit::put_SelFontSize](..\inked\nf-inked-iinkedit-put_selfontsize.md) | Gets or sets the font size of the selected text within the InkEdit control (run time only). |
| [IInkEdit::put_SelInksDisplayMode](..\inked\nf-inked-iinkedit-put_selinksdisplaymode.md) | Gets or sets a value that allows for toggling the appearance of the selection between ink and text. |
| [IInkEdit::put_SelInks](..\inked\nf-inked-iinkedit-put_selinks.md) | Gets or sets the array of embedded InkDisp objects (if displayed as ink) in the current selection. |
| [IInkEdit::put_SelItalic](..\inked\nf-inked-iinkedit-put_selitalic.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is italic (run time only). |
| [IInkEdit::put_SelLength](..\inked\nf-inked-iinkedit-put_sellength.md) | Gets or sets the number of characters that are selected in the InkEdit control (run time only). |
| [IInkEdit::put_SelRTF](..\inked\nf-inked-iinkedit-put_selrtf.md) | Gets or sets the currently selected Rich Text Format (RTF) formatted text in the InkEdit control (run time only). |
| [IInkEdit::put_SelStart](..\inked\nf-inked-iinkedit-put_selstart.md) | Gets or sets the starting point of the text that is selected in the InkEdit control (run time only). |
| [IInkEdit::put_SelText](..\inked\nf-inked-iinkedit-put_seltext.md) | Gets or sets the selected text within the InkEdit control (run time only). |
| [IInkEdit::put_SelUnderline](..\inked\nf-inked-iinkedit-put_selunderline.md) | Gets or sets a value that specifies whether the font style of the currently selected text in the InkEdit control is underlined (run time only). |
| [IInkEdit::put_TextRTF](..\inked\nf-inked-iinkedit-put_textrtf.md) | Gets or sets the text of the InkEdit control, including all RTF codes. |
| [IInkEdit::put_Text](..\inked\nf-inked-iinkedit-put_text.md) | Gets or sets the current text in the InkEdit control. |
| [IInkEdit::put_UseMouseForInput](..\inked\nf-inked-iinkedit-put_usemouseforinput.md) | Gets or sets a value that indicates whether the mouse can be used as an input device. |
| [IInkEdit::putref_DrawingAttributes](..\inked\nf-inked-iinkedit-putref_drawingattributes.md) | Gets or sets the drawing attributes for ink that is yet to be drawn on the InkEdit control. |
| [IInkExtendedProperties::Add](..\msinkaut\nf-msinkaut-iinkextendedproperties-add.md) | Creates and adds an IInkExtendedProperty object to the IInkExtendedProperties collection. |
| [IInkExtendedProperties::Clear](..\msinkaut\nf-msinkaut-iinkextendedproperties-clear.md) | Clears all of the IInkExtendedProperty objects from the IInkExtendedProperties collection. |
| [IInkExtendedProperties::DoesPropertyExist](..\msinkaut\nf-msinkaut-iinkextendedproperties-doespropertyexist.md) | Retrieves a value that indicates whether an IInkExtendedProperty object exists within an IInkExtendedProperties collection. |
| [IInkExtendedProperties::Item](..\msinkaut\nf-msinkaut-iinkextendedproperties-item.md) | Retrieves the IInkExtendedProperty object at the specified index within the IInkExtendedProperties collection. |
| [IInkExtendedProperties::Remove](..\msinkaut\nf-msinkaut-iinkextendedproperties-remove.md) | Removes the IInkExtendedProperty object from the IInkExtendedProperties collection. |
| [IInkExtendedProperties::get_Count](..\msinkaut\nf-msinkaut-iinkextendedproperties-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkExtendedProperty::get_Data](..\msinkaut\nf-msinkaut-iinkextendedproperty-get_data.md) | Gets or sets the data of the extended property. |
| [IInkExtendedProperty::get_Guid](..\msinkaut\nf-msinkaut-iinkextendedproperty-get_guid.md) | Gets the globally unique identifier (GUID) of the IInkExtendedProperty object. |
| [IInkExtendedProperty::put_Data](..\msinkaut\nf-msinkaut-iinkextendedproperty-put_data.md) | Gets or sets the data of the extended property. |
| [IInkGesture::GetHotPoint](..\msinkaut\nf-msinkaut-iinkgesture-gethotpoint.md) | Gets the hot point of the gesture, in ink space coordinates. |
| [IInkGesture::get_Confidence](..\msinkaut\nf-msinkaut-iinkgesture-get_confidence.md) | Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture. |
| [IInkGesture::get_Id](..\msinkaut\nf-msinkaut-iinkgesture-get_id.md) | Gets the identifier of an object. |
| [IInkLineInfo::GetCandidate](..\msinkaut\nf-msinkaut-iinklineinfo-getcandidate.md) | Returns one recognition alternate from the recognition result list. |
| [IInkLineInfo::GetFormat](..\msinkaut\nf-msinkaut-iinklineinfo-getformat.md) | Returns the display properties currently set on the text ink object (tInk). |
| [IInkLineInfo::GetInkExtent](..\msinkaut\nf-msinkaut-iinklineinfo-getinkextent.md) | Specifies the display properties to set on the text ink object (tInk), and retrieves the width of the text ink object in HIMETRIC units. |
| [IInkLineInfo::Recognize](..\msinkaut\nf-msinkaut-iinklineinfo-recognize.md) | Reserved. |
| [IInkLineInfo::SetCandidate](..\msinkaut\nf-msinkaut-iinklineinfo-setcandidate.md) | Updates one recognition alternate in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list. |
| [IInkLineInfo::SetFormat](..\msinkaut\nf-msinkaut-iinklineinfo-setformat.md) | Specifies the display properties to set on the text ink object (tInk). |
| [IInkOverlay::Draw](..\msinkaut\nf-msinkaut-iinkoverlay-draw.md) | Sets a rectangle in which to redraw the ink within the InkOverlay object. |
| [IInkOverlay::GetEventInterest](..\msinkaut\nf-msinkaut-iinkoverlay-geteventinterest.md) | Retrieves the interest an object has in a particular event for the InkCollector class, InkOverlay class, or InkPicture class. |
| [IInkOverlay::GetGestureStatus](..\msinkaut\nf-msinkaut-iinkoverlay-getgesturestatus.md) | Retrieves a value that determines whether the InkCollector or InkOverlay object is interested in a particular application gesture. |
| [IInkOverlay::GetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkoverlay-getwindowinputrectangle.md) | Gets the window rectangle, in pixels, within which ink is drawn. |
| [IInkOverlay::HitTestSelection](..\msinkaut\nf-msinkaut-iinkoverlay-hittestselection.md) | Determines what portion of the selection was hit during a hit test. |
| [IInkOverlay::SetAllTabletsMode](..\msinkaut\nf-msinkaut-iinkoverlay-setalltabletsmode.md) | Allows an ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from any tablet attached to the Tablet PC. |
| [IInkOverlay::SetEventInterest](..\msinkaut\nf-msinkaut-iinkoverlay-seteventinterest.md) | Sets a value that indicates whether an object or control has interest in a specified event. |
| [IInkOverlay::SetGestureStatus](..\msinkaut\nf-msinkaut-iinkoverlay-setgesturestatus.md) | Sets the interest of the object or control in a known gesture. |
| [IInkOverlay::SetSingleTabletIntegratedMode](..\msinkaut\nf-msinkaut-iinkoverlay-setsingletabletintegratedmode.md) | Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector. |
| [IInkOverlay::SetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkoverlay-setwindowinputrectangle.md) | Sets the window rectangle, in pixels, within which ink is drawn. |
| [IInkOverlay::get_AttachMode](..\msinkaut\nf-msinkaut-iinkoverlay-get_attachmode.md) | Gets or sets the value that specifies whether the InkOverlay object is attached behind or in front of the known window. |
| [IInkOverlay::get_AutoRedraw](..\msinkaut\nf-msinkaut-iinkoverlay-get_autoredraw.md) | Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated. |
| [IInkOverlay::get_CollectingInk](..\msinkaut\nf-msinkaut-iinkoverlay-get_collectingink.md) | Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). |
| [IInkOverlay::get_CollectionMode](..\msinkaut\nf-msinkaut-iinkoverlay-get_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. |
| [IInkOverlay::get_Cursors](..\msinkaut\nf-msinkaut-iinkoverlay-get_cursors.md) | Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device. |
| [IInkOverlay::get_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkoverlay-get_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkOverlay::get_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkoverlay-get_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkOverlay::get_DynamicRendering](..\msinkaut\nf-msinkaut-iinkoverlay-get_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkOverlay::get_EditingMode](..\msinkaut\nf-msinkaut-iinkoverlay-get_editingmode.md) | Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode. |
| [IInkOverlay::get_Enabled](..\msinkaut\nf-msinkaut-iinkoverlay-get_enabled.md) | Gets or sets a value that specifies whether the InkOverlay object collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkOverlay::get_EraserMode](..\msinkaut\nf-msinkaut-iinkoverlay-get_erasermode.md) | Gets or sets the value that specifies whether ink is erased by stroke or by point. |
| [IInkOverlay::get_EraserWidth](..\msinkaut\nf-msinkaut-iinkoverlay-get_eraserwidth.md) | Gets or sets the value that specifies the width of the eraser pen tip. |
| [IInkOverlay::get_Ink](..\msinkaut\nf-msinkaut-iinkoverlay-get_ink.md) | Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. |
| [IInkOverlay::get_MarginX](..\msinkaut\nf-msinkaut-iinkoverlay-get_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkOverlay::get_MarginY](..\msinkaut\nf-msinkaut-iinkoverlay-get_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkOverlay::get_MouseIcon](..\msinkaut\nf-msinkaut-iinkoverlay-get_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkOverlay::get_MousePointer](..\msinkaut\nf-msinkaut-iinkoverlay-get_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkOverlay::get_Renderer](..\msinkaut\nf-msinkaut-iinkoverlay-get_renderer.md) | Gets or sets the InkRenderer object that is used to draw ink. |
| [IInkOverlay::get_Selection](..\msinkaut\nf-msinkaut-iinkoverlay-get_selection.md) | Gets or sets the InkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control. |
| [IInkOverlay::get_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkoverlay-get_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkOverlay::get_SupportHighContrastSelectionUI](..\msinkaut\nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui.md) | Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode. |
| [IInkOverlay::get_Tablet](..\msinkaut\nf-msinkaut-iinkoverlay-get_tablet.md) | Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. |
| [IInkOverlay::get_hWnd](..\msinkaut\nf-msinkaut-iinkoverlay-get_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkOverlay::put_AttachMode](..\msinkaut\nf-msinkaut-iinkoverlay-put_attachmode.md) | Gets or sets the value that specifies whether the InkOverlay object is attached behind or in front of the known window. |
| [IInkOverlay::put_AutoRedraw](..\msinkaut\nf-msinkaut-iinkoverlay-put_autoredraw.md) | Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated. |
| [IInkOverlay::put_CollectionMode](..\msinkaut\nf-msinkaut-iinkoverlay-put_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gesture, or both are recognized as the user writes. |
| [IInkOverlay::put_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkoverlay-put_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkOverlay::put_DynamicRendering](..\msinkaut\nf-msinkaut-iinkoverlay-put_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkOverlay::put_EditingMode](..\msinkaut\nf-msinkaut-iinkoverlay-put_editingmode.md) | Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode. |
| [IInkOverlay::put_Enabled](..\msinkaut\nf-msinkaut-iinkoverlay-put_enabled.md) | Gets or sets a value that specifies whether the InkOverlay object collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkOverlay::put_EraserMode](..\msinkaut\nf-msinkaut-iinkoverlay-put_erasermode.md) | Gets or sets the value that specifies whether ink is erased by stroke or by point. |
| [IInkOverlay::put_EraserWidth](..\msinkaut\nf-msinkaut-iinkoverlay-put_eraserwidth.md) | Gets or sets the value that specifies the width of the eraser pen tip. |
| [IInkOverlay::put_MarginX](..\msinkaut\nf-msinkaut-iinkoverlay-put_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkOverlay::put_MarginY](..\msinkaut\nf-msinkaut-iinkoverlay-put_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkOverlay::put_MouseIcon](..\msinkaut\nf-msinkaut-iinkoverlay-put_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkOverlay::put_MousePointer](..\msinkaut\nf-msinkaut-iinkoverlay-put_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkOverlay::put_Selection](..\msinkaut\nf-msinkaut-iinkoverlay-put_selection.md) | Gets or sets the InkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control. |
| [IInkOverlay::put_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkoverlay-put_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkOverlay::put_SupportHighContrastSelectionUI](..\msinkaut\nf-msinkaut-iinkoverlay-put_supporthighcontrastselectionui.md) | Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode. |
| [IInkOverlay::put_hWnd](..\msinkaut\nf-msinkaut-iinkoverlay-put_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkPicture::GetEventInterest](..\msinkaut\nf-msinkaut-iinkpicture-geteventinterest.md) | Retrieves the interest an object has in a particular event for the InkCollector class, InkOverlay class, or InkPicture class. |
| [IInkPicture::GetGestureStatus](..\msinkaut\nf-msinkaut-iinkpicture-getgesturestatus.md) | Retrieves a value that indicates whether the InkPicture control has interest in a particular application gesture. |
| [IInkPicture::GetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkpicture-getwindowinputrectangle.md) | Retrieves the window rectangle, in pixels, within which ink is drawn. |
| [IInkPicture::HitTestSelection](..\msinkaut\nf-msinkaut-iinkpicture-hittestselection.md) | Retrieves a member of the SelectionHitResult enumeration, which specifies which part of a selection, if any, was hit during a hit test. |
| [IInkPicture::SetAllTabletsMode](..\msinkaut\nf-msinkaut-iinkpicture-setalltabletsmode.md) | Allows an ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from any tablet attached to the Tablet PC. |
| [IInkPicture::SetEventInterest](..\msinkaut\nf-msinkaut-iinkpicture-seteventinterest.md) | Modifies a value that indicates whether an object or control has interest in a specified event. |
| [IInkPicture::SetGestureStatus](..\msinkaut\nf-msinkaut-iinkpicture-setgesturestatus.md) | Modifies the interest of the object or control in a known gesture. |
| [IInkPicture::SetSingleTabletIntegratedMode](..\msinkaut\nf-msinkaut-iinkpicture-setsingletabletintegratedmode.md) | Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector. |
| [IInkPicture::SetWindowInputRectangle](..\msinkaut\nf-msinkaut-iinkpicture-setwindowinputrectangle.md) | Modifies the window rectangle, in pixels, within which ink is drawn. |
| [IInkPicture::get_AutoRedraw](..\msinkaut\nf-msinkaut-iinkpicture-get_autoredraw.md) | Gets or sets a value that specifies whether an ink collectcor repaints the ink when the window is invalidated. |
| [IInkPicture::get_BackColor](..\msinkaut\nf-msinkaut-iinkpicture-get_backcolor.md) | Gets or sets the background color for the InkPicture control. |
| [IInkPicture::get_CollectingInk](..\msinkaut\nf-msinkaut-iinkpicture-get_collectingink.md) | Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). |
| [IInkPicture::get_CollectionMode](..\msinkaut\nf-msinkaut-iinkpicture-get_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gestures, or both are recognized as the user writes. |
| [IInkPicture::get_Cursors](..\msinkaut\nf-msinkaut-iinkpicture-get_cursors.md) | Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device. |
| [IInkPicture::get_DefaultDrawingAttributes](..\msinkaut\nf-msinkaut-iinkpicture-get_defaultdrawingattributes.md) | Gets or sets the default drawing attributes to use when drawing and displaying ink. |
| [IInkPicture::get_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkpicture-get_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkPicture::get_DynamicRendering](..\msinkaut\nf-msinkaut-iinkpicture-get_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkPicture::get_EditingMode](..\msinkaut\nf-msinkaut-iinkpicture-get_editingmode.md) | Gets or sets a value that specifies whether the InkPicture control is in ink mode, deletion mode, or selecting/editing mode. |
| [IInkPicture::get_Enabled](..\msinkaut\nf-msinkaut-iinkpicture-get_enabled.md) | Gets or sets a value that determines whether the InkPicture control can respond to user-generated events. |
| [IInkPicture::get_EraserMode](..\msinkaut\nf-msinkaut-iinkpicture-get_erasermode.md) | Gets or sets a value that specifies whether ink is erased by stroke or by point. |
| [IInkPicture::get_EraserWidth](..\msinkaut\nf-msinkaut-iinkpicture-get_eraserwidth.md) | Gets or sets a value that specifies the width of the eraser pen tip. |
| [IInkPicture::get_InkEnabled](..\msinkaut\nf-msinkaut-iinkpicture-get_inkenabled.md) | Gets or sets a value that specifies whether the InkPicture control collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkPicture::get_Ink](..\msinkaut\nf-msinkaut-iinkpicture-get_ink.md) | Gets or sets the InkDisp object that is associated with the InkPicture control. |
| [IInkPicture::get_MarginX](..\msinkaut\nf-msinkaut-iinkpicture-get_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkPicture::get_MarginY](..\msinkaut\nf-msinkaut-iinkpicture-get_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkPicture::get_MouseIcon](..\msinkaut\nf-msinkaut-iinkpicture-get_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkPicture::get_MousePointer](..\msinkaut\nf-msinkaut-iinkpicture-get_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkPicture::get_Picture](..\msinkaut\nf-msinkaut-iinkpicture-get_picture.md) | Gets the graphics file to appear on the InkPicture control. |
| [IInkPicture::get_Renderer](..\msinkaut\nf-msinkaut-iinkpicture-get_renderer.md) | Gets or sets the InkRenderer object that is used to draw ink. |
| [IInkPicture::get_Selection](..\msinkaut\nf-msinkaut-iinkpicture-get_selection.md) | Gets or sets theInkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control. |
| [IInkPicture::get_SizeMode](..\msinkaut\nf-msinkaut-iinkpicture-get_sizemode.md) | Gets or sets how the InkPicture control handles image placement and sizing. |
| [IInkPicture::get_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkpicture-get_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkPicture::get_SupportHighContrastSelectionUI](..\msinkaut\nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui.md) | Gets or sets a value that specifies whether all selection user interface (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode. |
| [IInkPicture::get_Tablet](..\msinkaut\nf-msinkaut-iinkpicture-get_tablet.md) | Gets either the IInkTablet object to which a cursor belongs or the IInkTablet object that an object or control is currently using to collect input. |
| [IInkPicture::get_hWnd](..\msinkaut\nf-msinkaut-iinkpicture-get_hwnd.md) | Gets or sets the handle value of the window on which ink is drawn. |
| [IInkPicture::put_AutoRedraw](..\msinkaut\nf-msinkaut-iinkpicture-put_autoredraw.md) | Gets or sets a value that specifies whether an ink collectcor repaints the ink when the window is invalidated. |
| [IInkPicture::put_BackColor](..\msinkaut\nf-msinkaut-iinkpicture-put_backcolor.md) | Gets or sets the background color for the InkPicture control. |
| [IInkPicture::put_CollectionMode](..\msinkaut\nf-msinkaut-iinkpicture-put_collectionmode.md) | Gets or sets the collection mode that determines whether ink, gestures, or both are recognized as the user writes. |
| [IInkPicture::put_DesiredPacketDescription](..\msinkaut\nf-msinkaut-iinkpicture-put_desiredpacketdescription.md) | Gets or sets the desired packet description of the InkCollector. |
| [IInkPicture::put_DynamicRendering](..\msinkaut\nf-msinkaut-iinkpicture-put_dynamicrendering.md) | Gets or sets the value that specifies whether ink is rendered as it is drawn. |
| [IInkPicture::put_EditingMode](..\msinkaut\nf-msinkaut-iinkpicture-put_editingmode.md) | Gets or sets a value that specifies whether the InkPicture control is in ink mode, deletion mode, or selecting/editing mode. |
| [IInkPicture::put_Enabled](..\msinkaut\nf-msinkaut-iinkpicture-put_enabled.md) | Gets or sets a value that determines whether the InkPicture control can respond to user-generated events. |
| [IInkPicture::put_EraserMode](..\msinkaut\nf-msinkaut-iinkpicture-put_erasermode.md) | Gets or sets a value that specifies whether ink is erased by stroke or by point. |
| [IInkPicture::put_EraserWidth](..\msinkaut\nf-msinkaut-iinkpicture-put_eraserwidth.md) | Gets or sets a value that specifies the width of the eraser pen tip. |
| [IInkPicture::put_InkEnabled](..\msinkaut\nf-msinkaut-iinkpicture-put_inkenabled.md) | Gets or sets a value that specifies whether the InkPicture control collects pen input (in-air packets, cursor in range events, and so on). |
| [IInkPicture::put_MarginX](..\msinkaut\nf-msinkaut-iinkpicture-put_marginx.md) | Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkPicture::put_MarginY](..\msinkaut\nf-msinkaut-iinkpicture-put_marginy.md) | Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. |
| [IInkPicture::put_MouseIcon](..\msinkaut\nf-msinkaut-iinkpicture-put_mouseicon.md) | Gets or sets the custom mouse icon. |
| [IInkPicture::put_MousePointer](..\msinkaut\nf-msinkaut-iinkpicture-put_mousepointer.md) | Gets or sets a value that indicates the type of mouse pointer that appears. |
| [IInkPicture::put_Picture](..\msinkaut\nf-msinkaut-iinkpicture-put_picture.md) | Gets the graphics file to appear on the InkPicture control. |
| [IInkPicture::put_Selection](..\msinkaut\nf-msinkaut-iinkpicture-put_selection.md) | Gets or sets theInkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control. |
| [IInkPicture::put_SizeMode](..\msinkaut\nf-msinkaut-iinkpicture-put_sizemode.md) | Gets or sets how the InkPicture control handles image placement and sizing. |
| [IInkPicture::put_SupportHighContrastInk](..\msinkaut\nf-msinkaut-iinkpicture-put_supporthighcontrastink.md) | Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode. |
| [IInkPicture::put_SupportHighContrastSelectionUI](..\msinkaut\nf-msinkaut-iinkpicture-put_supporthighcontrastselectionui.md) | Gets or sets a value that specifies whether all selection user interface (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode. |
| [IInkRecognitionAlternate::AlternatesWithConstantPropertyValues](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues.md) | Retrieves a IInkRecognitionAlternates collection, which are a division of the IInkRecognitionAlternate object on which this method is called. |
| [IInkRecognitionAlternate::GetPropertyValue](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getpropertyvalue.md) | Retrieves the value of a specified property of the alternate. |
| [IInkRecognitionAlternate::GetStrokesFromStrokeRanges](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getstrokesfromstrokeranges.md) | Retrieves the smallest InkStrokes collection that contains a known input InkStrokes collection and for which the IInkRecognizer object can provide alternates. |
| [IInkRecognitionAlternate::GetStrokesFromTextRange](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-getstrokesfromtextrange.md) | Retrives the collection that corresponds to the smallest set of recognition segments that contains a specified character range within the alternate. |
| [IInkRecognitionAlternate::GetTextRangeFromStrokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-gettextrangefromstrokes.md) | Retrieves the smallest range of recognized text for which the recognizer can return an alternate that contains a known InkStrokes collection. |
| [IInkRecognitionAlternate::get_Ascender](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_ascender.md) | Gets the ascender line for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_Baseline](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_baseline.md) | Gets the baseline for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_ConfidenceAlternates](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_confidencealternates.md) | Gets the collection of alternates in which each alternate in the collection consists of the segments with the same property values. |
| [IInkRecognitionAlternate::get_Confidence](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_confidence.md) | Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture. |
| [IInkRecognitionAlternate::get_Descender](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_descender.md) | Gets the decender line for an IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_LineAlternates](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_linealternates.md) | Gets the IInkRecognitionAlternates collection in which each alternate in the collection is on a separate line. |
| [IInkRecognitionAlternate::get_LineNumber](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_linenumber.md) | Gets the line number of the ink that makes up the alternate. |
| [IInkRecognitionAlternate::get_Midline](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_midline.md) | Gets the midline for a IInkRecognitionAlternate object that represents a single line of text. |
| [IInkRecognitionAlternate::get_String](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_string.md) | Gets the top string of the alternate. |
| [IInkRecognitionAlternate::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternate-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionAlternates::Item](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-item.md) | Retrieves the IInkRecognitionAlternate object at the specified index within the IInkRecognitionAlternates collection. |
| [IInkRecognitionAlternates::get_Count](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkRecognitionAlternates::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionalternates-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionResult::ModifyTopAlternate](..\msinkaut\nf-msinkaut-iinkrecognitionresult-modifytopalternate.md) | Changes the top alternate of a recognition result by using the specified alternate. |
| [IInkRecognitionResult::SetResultOnStrokes](..\msinkaut\nf-msinkaut-iinkrecognitionresult-setresultonstrokes.md) | Assigns the recognition results to the strokes that were used to create the results. |
| [IInkRecognitionResult::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_strokes.md) | Gets the collection of strokes that are contained in an object or used to create an object. |
| [IInkRecognitionResult::get_TopAlternate](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topalternate.md) | Gets the top alternate of the recognition result. |
| [IInkRecognitionResult::get_TopConfidence](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topconfidence.md) | Gets the top alternate of the recognition result. |
| [IInkRecognitionResult::get_TopString](..\msinkaut\nf-msinkaut-iinkrecognitionresult-get_topstring.md) | Gets the result text for the TopAlternate property. |
| [IInkRecognizer2::get_Id](..\msinkaut\nf-msinkaut-iinkrecognizer2-get_id.md) | Retrieves the ID for the InkRecognizer. |
| [IInkRecognizer2::get_UnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizer2-get_unicoderanges.md) | Retrieves the Unicode ranges set for the current recognizer. |
| [IInkRecognizer::CreateRecognizerContext](..\msinkaut\nf-msinkaut-iinkrecognizer-createrecognizercontext.md) | Creates a new InkRecognizerContext object. |
| [IInkRecognizer::get_Capabilities](..\msinkaut\nf-msinkaut-iinkrecognizer-get_capabilities.md) | Gets the capabilities of the IInkRecognizer object. |
| [IInkRecognizer::get_Languages](..\msinkaut\nf-msinkaut-iinkrecognizer-get_languages.md) | Gets an array of language identifiers for the languages that the IInkRecognizer object supports. |
| [IInkRecognizer::get_Name](..\msinkaut\nf-msinkaut-iinkrecognizer-get_name.md) | Gets the name of the object. |
| [IInkRecognizer::get_PreferredPacketDescription](..\msinkaut\nf-msinkaut-iinkrecognizer-get_preferredpacketdescription.md) | Gets an array of globally unique identifiers (GUIDs) that represents the preferred packet properties for the recognizer. |
| [IInkRecognizer::get_SupportedProperties](..\msinkaut\nf-msinkaut-iinkrecognizer-get_supportedproperties.md) | Gets an array of globally unique identifiers (GUIDs) that describe the properties that the IInkRecognizer object supports. |
| [IInkRecognizer::get_Vendor](..\msinkaut\nf-msinkaut-iinkrecognizer-get_vendor.md) | Gets the vendor name of the IInkRecognizer object. |
| [IInkRecognizerContext2::get_EnabledUnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizercontext2-get_enabledunicoderanges.md) | Gets or sets a set of one or more Unicode ranges that the recognizer context will support. |
| [IInkRecognizerContext2::put_EnabledUnicodeRanges](..\msinkaut\nf-msinkaut-iinkrecognizercontext2-put_enabledunicoderanges.md) | Gets or sets a set of one or more Unicode ranges that the recognizer context will support. |
| [IInkRecognizerContext::BackgroundRecognizeWithAlternates](..\msinkaut\nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates.md) | Causes the IInkRecognizer object to recognize the associated strokes collection and fire a RecognitionWithAlternates event when recognition is complete. |
| [IInkRecognizerContext::BackgroundRecognize](..\msinkaut\nf-msinkaut-iinkrecognizercontext-backgroundrecognize.md) | Causes the IInkRecognizer object to recognize the associated strokes collection and fire a Recognition event when recognition is complete. |
| [IInkRecognizerContext::Clone](..\msinkaut\nf-msinkaut-iinkrecognizercontext-clone.md) | Creates a duplicate InkRecognizerContext object. |
| [IInkRecognizerContext::EndInkInput](..\msinkaut\nf-msinkaut-iinkrecognizercontext-endinkinput.md) | EndInkInput is no longer available for use for recognizers of western languages as of Windows Vista. |
| [IInkRecognizerContext::IsStringSupported](..\msinkaut\nf-msinkaut-iinkrecognizercontext-isstringsupported.md) | Indicates whether the system dictionary, user dictionary, or word list contain a specified string. |
| [IInkRecognizerContext::Recognize](..\msinkaut\nf-msinkaut-iinkrecognizercontext-recognize.md) | Performs recognition on an InkStrokes collection and returns recognition results. |
| [IInkRecognizerContext::StopBackgroundRecognition](..\msinkaut\nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition.md) | Ends background recognition that was started with a call to BackgroundRecognize or BackgroundRecognizeWithAlternates. |
| [IInkRecognizerContext::get_Factoid](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_factoid.md) | Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result. |
| [IInkRecognizerContext::get_Guide](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_guide.md) | Gets or sets the InkRecognizerGuide to use for ink input. |
| [IInkRecognizerContext::get_PrefixText](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_prefixtext.md) | Gets or sets the characters that come before the InkStrokes collection in the InkRecognizerContext object. |
| [IInkRecognizerContext::get_RecognitionFlags](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_recognitionflags.md) | Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string. |
| [IInkRecognizerContext::get_Recognizer](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_recognizer.md) | Gets the IInkRecognizer object used by the InkRecognizerContext object. |
| [IInkRecognizerContext::get_Strokes](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_strokes.md) | Gets or sets the InkStrokes collection associated with the InkRecognizerContext object. |
| [IInkRecognizerContext::get_SuffixText](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_suffixtext.md) | Gets or sets the characters that come after the InkStrokes collection in the InkRecognizerContext object. |
| [IInkRecognizerContext::get_WordList](..\msinkaut\nf-msinkaut-iinkrecognizercontext-get_wordlist.md) | Gets or sets the word list that is used in the recognition process to improve the recognition results. |
| [IInkRecognizerContext::put_Factoid](..\msinkaut\nf-msinkaut-iinkrecognizercontext-put_factoid.md) | Gets or sets the factoid that a recognizer uses to constrain its search for the recognition result. |
| [IInkRecognizerContext::put_PrefixText](..\msinkaut\nf-msinkaut-iinkrecognizercontext-put_prefixtext.md) | Gets or sets the characters that come before the InkStrokes collection in the InkRecognizerContext object. |
| [IInkRecognizerContext::put_RecognitionFlags](..\msinkaut\nf-msinkaut-iinkrecognizercontext-put_recognitionflags.md) | Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string. |
| [IInkRecognizerContext::put_SuffixText](..\msinkaut\nf-msinkaut-iinkrecognizercontext-put_suffixtext.md) | Gets or sets the characters that come after the InkStrokes collection in the InkRecognizerContext object. |
| [IInkRecognizerContext::putref_Guide](..\msinkaut\nf-msinkaut-iinkrecognizercontext-putref_guide.md) | Gets or sets the InkRecognizerGuide to use for ink input. |
| [IInkRecognizerContext::putref_Strokes](..\msinkaut\nf-msinkaut-iinkrecognizercontext-putref_strokes.md) | Gets or sets the InkStrokes collection associated with the InkRecognizerContext object. |
| [IInkRecognizerContext::putref_WordList](..\msinkaut\nf-msinkaut-iinkrecognizercontext-putref_wordlist.md) | Gets or sets the word list that is used in the recognition process to improve the recognition results. |
| [IInkRecognizerGuide::get_Columns](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_columns.md) | Gets or sets the number of columns in the recognition guide box. |
| [IInkRecognizerGuide::get_DrawnBox](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_drawnbox.md) | Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place. |
| [IInkRecognizerGuide::get_GuideData](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_guidedata.md) | Gets or sets the InkRecoGuide structure that represents the boundaries of the ink to the recognizer. |
| [IInkRecognizerGuide::get_Midline](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_midline.md) | Gets or sets the midline height. The midline height is distance from the baseline to the midline, of the drawn box. |
| [IInkRecognizerGuide::get_Rows](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_rows.md) | Gets or sets the number of rows in the recognition guide. |
| [IInkRecognizerGuide::get_WritingBox](..\msinkaut\nf-msinkaut-iinkrecognizerguide-get_writingbox.md) | Gets or sets the invisible writing area of the recognition guide in which writing can actually take place. |
| [IInkRecognizerGuide::put_Columns](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_columns.md) | Gets or sets the number of columns in the recognition guide box. |
| [IInkRecognizerGuide::put_DrawnBox](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_drawnbox.md) | Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place. |
| [IInkRecognizerGuide::put_GuideData](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_guidedata.md) | Gets or sets the InkRecoGuide structure that represents the boundaries of the ink to the recognizer. |
| [IInkRecognizerGuide::put_Midline](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_midline.md) | Gets or sets the midline height. The midline height is distance from the baseline to the midline, of the drawn box. |
| [IInkRecognizerGuide::put_Rows](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_rows.md) | Gets or sets the number of rows in the recognition guide. |
| [IInkRecognizerGuide::put_WritingBox](..\msinkaut\nf-msinkaut-iinkrecognizerguide-put_writingbox.md) | Gets or sets the invisible writing area of the recognition guide in which writing can actually take place. |
| [IInkRecognizers::GetDefaultRecognizer](..\msinkaut\nf-msinkaut-iinkrecognizers-getdefaultrecognizer.md) | Retrieves the default recognizer for a known language, specified by a national language support (NLS) language code identifier (LCID). |
| [IInkRecognizers::Item](..\msinkaut\nf-msinkaut-iinkrecognizers-item.md) | Retrieves the IInkRecognizer object at the specified index within the InkRecognizers collection. |
| [IInkRecognizers::get_Count](..\msinkaut\nf-msinkaut-iinkrecognizers-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkRectangle::GetRectangle](..\msinkaut\nf-msinkaut-iinkrectangle-getrectangle.md) | Gets the elements of the InkRectangle object in a single call. |
| [IInkRectangle::SetRectangle](..\msinkaut\nf-msinkaut-iinkrectangle-setrectangle.md) | Sets the elements of the InkRectangle object in a single call. |
| [IInkRectangle::get_Bottom](..\msinkaut\nf-msinkaut-iinkrectangle-get_bottom.md) | Gets or sets the bottom position of the InkRectangle object. |
| [IInkRectangle::get_Data](..\msinkaut\nf-msinkaut-iinkrectangle-get_data.md) | Gets or sets access to the rectangle structure (C++ only). |
| [IInkRectangle::get_Left](..\msinkaut\nf-msinkaut-iinkrectangle-get_left.md) | Gets or sets the left position of the InkRectangle object. |
| [IInkRectangle::get_Right](..\msinkaut\nf-msinkaut-iinkrectangle-get_right.md) | Gets or sets the right position of the InkRectangle object. |
| [IInkRectangle::get_Top](..\msinkaut\nf-msinkaut-iinkrectangle-get_top.md) | Gets or sets the top position of the InkRectangle object. |
| [IInkRectangle::put_Bottom](..\msinkaut\nf-msinkaut-iinkrectangle-put_bottom.md) | Gets or sets the bottom position of the InkRectangle object. |
| [IInkRectangle::put_Data](..\msinkaut\nf-msinkaut-iinkrectangle-put_data.md) | Gets or sets access to the rectangle structure (C++ only). |
| [IInkRectangle::put_Left](..\msinkaut\nf-msinkaut-iinkrectangle-put_left.md) | Gets or sets the left position of the InkRectangle object. |
| [IInkRectangle::put_Right](..\msinkaut\nf-msinkaut-iinkrectangle-put_right.md) | Gets or sets the right position of the InkRectangle object. |
| [IInkRectangle::put_Top](..\msinkaut\nf-msinkaut-iinkrectangle-put_top.md) | Gets or sets the top position of the InkRectangle object. |
| [IInkRenderer::DrawStroke](..\msinkaut\nf-msinkaut-iinkrenderer-drawstroke.md) | Draws the IInkStrokeDisp object using the known device context, and optionally draws the IInkStrokeDisp object with the known InkDrawingAttributes object. |
| [IInkRenderer::Draw](..\msinkaut\nf-msinkaut-iinkrenderer-draw.md) | Draws ink strokes using the known device context. |
| [IInkRenderer::GetObjectTransform](..\msinkaut\nf-msinkaut-iinkrenderer-getobjecttransform.md) | Gets the InkTransform object that represents the object transform that was used to render ink. |
| [IInkRenderer::GetViewTransform](..\msinkaut\nf-msinkaut-iinkrenderer-getviewtransform.md) | Gets the InkTransform object that represents the view transform that is used to render ink. |
| [IInkRenderer::InkSpaceToPixelFromPoints](..\msinkaut\nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints.md) | Converts an array of points in ink space coordinates to an array of points in pixel space. |
| [IInkRenderer::InkSpaceToPixel](..\msinkaut\nf-msinkaut-iinkrenderer-inkspacetopixel.md) | Converts a location in ink space coordinates to a location in pixel space using a handle for the conversion. |
| [IInkRenderer::Measure](..\msinkaut\nf-msinkaut-iinkrenderer-measure.md) | Calculates the rectangle on the device context that would contain a collection of strokes if the strokes were drawn with the InkRenderer object using the DrawStroke method. |
| [IInkRenderer::Move](..\msinkaut\nf-msinkaut-iinkrenderer-move.md) | Applies a translation to the view transform in ink space coordinates. |
| [IInkRenderer::PixelToInkSpaceFromPoints](..\msinkaut\nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints.md) | Converts an array of locations in pixel space coordinates to an array of locations in ink space coordinates. |
| [IInkRenderer::PixelToInkSpace](..\msinkaut\nf-msinkaut-iinkrenderer-pixeltoinkspace.md) | Converts a location in pixel space coordinates to be a location in ink space coordinates. |
| [IInkRenderer::Rotate](..\msinkaut\nf-msinkaut-iinkrenderer-rotate.md) | Applies a rotation to a InkRenderer's view transform. |
| [IInkRenderer::ScaleTransform](..\msinkaut\nf-msinkaut-iinkrenderer-scaletransform.md) | Scales the view transform in the X and Y dimension. |
| [IInkRenderer::SetObjectTransform](..\msinkaut\nf-msinkaut-iinkrenderer-setobjecttransform.md) | Sets the InkTransform object that represents the object transform that is used to render ink. |
| [IInkRenderer::SetViewTransform](..\msinkaut\nf-msinkaut-iinkrenderer-setviewtransform.md) | Sets the InkTransform object that represents the view transform that is used to render ink. |
| [IInkStrokeDisp::Clip](..\msinkaut\nf-msinkaut-iinkstrokedisp-clip.md) | Removes portions of an IInkStrokeDisp object or InkStrokes collection that are outside a rectangle. |
| [IInkStrokeDisp::FindIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-findintersections.md) | Retrieves the points where this IInkStrokeDisp object intersects other IInkStrokeDisp objects within a known InkStrokes collection. |
| [IInkStrokeDisp::GetBoundingBox](..\msinkaut\nf-msinkaut-iinkstrokedisp-getboundingbox.md) | Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection. |
| [IInkStrokeDisp::GetFlattenedBezierPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-getflattenedbezierpoints.md) | Retrieves the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or a InkStrokes collection. |
| [IInkStrokeDisp::GetPacketData](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketdata.md) | Retrieves the packet data for a range of packets within the IInkStrokeDisp object. |
| [IInkStrokeDisp::GetPacketDescriptionPropertyMetrics](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics.md) | Retrieves the metrics for a given packet description type. |
| [IInkStrokeDisp::GetPacketValuesByProperty](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty.md) | Retrieves the data for a known packet property from one or more packets in the stroke. |
| [IInkStrokeDisp::GetPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-getpoints.md) | Retrieves the points that make up a stroke. |
| [IInkStrokeDisp::GetRectangleIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-getrectangleintersections.md) | Finds the points where a IInkStrokeDisp object intersects a given rectangle. |
| [IInkStrokeDisp::HitTestCircle](..\msinkaut\nf-msinkaut-iinkstrokedisp-hittestcircle.md) | Determines whether a stroke is either completely inside or intersected by a given circle. |
| [IInkStrokeDisp::Move](..\msinkaut\nf-msinkaut-iinkstrokedisp-move.md) | Applies a translation to the ink of an IInkStrokeDisp object or InkStrokes collection. |
| [IInkStrokeDisp::NearestPoint](..\msinkaut\nf-msinkaut-iinkstrokedisp-nearestpoint.md) | Finds the location on the stroke nearest to a known point and returns the distance that point is from the stroke. Everything is in ink space coordinates. |
| [IInkStrokeDisp::Rotate](..\msinkaut\nf-msinkaut-iinkstrokedisp-rotate.md) | Rotates the ink using an angle in degrees around a center point of the rotation. |
| [IInkStrokeDisp::ScaleToRectangle](..\msinkaut\nf-msinkaut-iinkstrokedisp-scaletorectangle.md) | Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object. |
| [IInkStrokeDisp::ScaleTransform](..\msinkaut\nf-msinkaut-iinkstrokedisp-scaletransform.md) | Applies the specified horizontal and vertical factors to the transform or ink. |
| [IInkStrokeDisp::SetPacketValuesByProperty](..\msinkaut\nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty.md) | Modifies the packet values for a particular property. |
| [IInkStrokeDisp::SetPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-setpoints.md) | Sets the points of the IInkStrokeDisp using an array of X, Y values. |
| [IInkStrokeDisp::Shear](..\msinkaut\nf-msinkaut-iinkstrokedisp-shear.md) | Shears the ink in the stroke or strokes by the specified horizontal and vertical factors. |
| [IInkStrokeDisp::Split](..\msinkaut\nf-msinkaut-iinkstrokedisp-split.md) | Splits the stroke at the specified location on the stroke. |
| [IInkStrokeDisp::Transform](..\msinkaut\nf-msinkaut-iinkstrokedisp-transform.md) | Applies a linear transformation to an IInkStrokeDisp object or an InkStrokes collection, which can represent scaling, rotation, translation, and combinations of transformations. |
| [IInkStrokeDisp::get_BezierCusps](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_beziercusps.md) | Gets an array that contains the indices of the cusps of the Bezier approximation of the stroke. |
| [IInkStrokeDisp::get_BezierPoints](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_bezierpoints.md) | Gets the array of control points that represent the Bezier approximation of the stroke. |
| [IInkStrokeDisp::get_Deleted](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_deleted.md) | Gets a value that specifies whether a known stroke is deleted from the ink. |
| [IInkStrokeDisp::get_DrawingAttributes](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_drawingattributes.md) | Gets or sets the drawing attributes to apply to ink as it is drawn. |
| [IInkStrokeDisp::get_ExtendedProperties](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_extendedproperties.md) | Gets the collection of application-defined data that are stored in an object. |
| [IInkStrokeDisp::get_ID](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_id.md) | Gets the identifier of an object. |
| [IInkStrokeDisp::get_Ink](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_ink.md) | Gets the parent InkDisp object of a stroke. |
| [IInkStrokeDisp::get_PacketCount](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetcount.md) | Gets the number of packets received for an IInkStrokeDisp object. |
| [IInkStrokeDisp::get_PacketDescription](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetdescription.md) | Gets an array of globally unique identifiers (GUIDs) that describes the types of packet data stored in the IInkStrokeDisp object. |
| [IInkStrokeDisp::get_PacketSize](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_packetsize.md) | Gets the size, in bytes, of a packet. |
| [IInkStrokeDisp::get_PolylineCusps](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_polylinecusps.md) | Gets an array that contains the indices of the cusps of the IInkStrokeDisp object. |
| [IInkStrokeDisp::get_SelfIntersections](..\msinkaut\nf-msinkaut-iinkstrokedisp-get_selfintersections.md) | Gets the self-intersections of the stroke. |
| [IInkStrokes::AddStrokes](..\msinkaut\nf-msinkaut-iinkstrokes-addstrokes.md) | Adds a Strokes collection to an existing Strokes collection. |
| [IInkStrokes::Add](..\msinkaut\nf-msinkaut-iinkstrokes-add.md) | Adds an IInkStrokeDisp object or InkStrokes collection to an existing InkStrokes collection. |
| [IInkStrokes::Clip](..\msinkaut\nf-msinkaut-iinkstrokes-clip.md) | Removes portions of an IInkStrokeDisp object or InkStrokes collection that are outside a rectangle. |
| [IInkStrokes::GetBoundingBox](..\msinkaut\nf-msinkaut-iinkstrokes-getboundingbox.md) | Gets the bounding box in ink space coordinates for either all of the strokes in an InkDisp object, an individual stroke, or an InkStrokes collection. |
| [IInkStrokes::Item](..\msinkaut\nf-msinkaut-iinkstrokes-item.md) | Retrieves the IInkStrokeDisp object at the specified index within the InkStrokes collection. |
| [IInkStrokes::ModifyDrawingAttributes](..\msinkaut\nf-msinkaut-iinkstrokes-modifydrawingattributes.md) | Sets the drawing attributes of all of the strokes in an InkStrokes collection. |
| [IInkStrokes::Move](..\msinkaut\nf-msinkaut-iinkstrokes-move.md) | Applies a translation to the ink of an IInkStrokeDisp object or InkStrokes collection. |
| [IInkStrokes::RemoveRecognitionResult](..\msinkaut\nf-msinkaut-iinkstrokes-removerecognitionresult.md) | Removes the RecognitionResult that is associated with the InkStrokes collection. |
| [IInkStrokes::RemoveStrokes](..\msinkaut\nf-msinkaut-iinkstrokes-removestrokes.md) | Removes strokes from the collection. |
| [IInkStrokes::Remove](..\msinkaut\nf-msinkaut-iinkstrokes-remove.md) | Removes an IInkStrokeDisp object from a InkStrokes collection. |
| [IInkStrokes::Rotate](..\msinkaut\nf-msinkaut-iinkstrokes-rotate.md) | Rotates the ink using an angle in degrees around a center point of the rotation. |
| [IInkStrokes::ScaleToRectangle](..\msinkaut\nf-msinkaut-iinkstrokes-scaletorectangle.md) | Scales the IInkStrokeDisp object or InkStrokes collection to fit in the specified InkRectangle object. |
| [IInkStrokes::ScaleTransform](..\msinkaut\nf-msinkaut-iinkstrokes-scaletransform.md) | Applies the specified horizontal and vertical factors to the transform or ink. |
| [IInkStrokes::Shear](..\msinkaut\nf-msinkaut-iinkstrokes-shear.md) | Shears the ink in the stroke or strokes by the specified horizontal and vertical factors. |
| [IInkStrokes::ToString](..\msinkaut\nf-msinkaut-iinkstrokes-tostring.md) | ToString is no longer available for use as of Windows Vista. |
| [IInkStrokes::Transform](..\msinkaut\nf-msinkaut-iinkstrokes-transform.md) | Applies a linear transformation to an IInkStrokeDisp object or an InkStrokes collection, which can represent scaling, rotation, translation, and combinations of transformations. |
| [IInkStrokes::get_Count](..\msinkaut\nf-msinkaut-iinkstrokes-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkStrokes::get_Ink](..\msinkaut\nf-msinkaut-iinkstrokes-get_ink.md) | Gets the InkDisp object that contains a collection of strokes. |
| [IInkStrokes::get_RecognitionResult](..\msinkaut\nf-msinkaut-iinkstrokes-get_recognitionresult.md) | Gets the IInkRecognitionResult object of the InkStrokes collection. |
| [IInkTablet2::get_DeviceKind](..\msinkaut\nf-msinkaut-iinktablet2-get_devicekind.md) | Gets the type of Tablet device being used. |
| [IInkTablet3::get_IsMultiTouch](..\msinkaut\nf-msinkaut-iinktablet3-get_ismultitouch.md) | Gets a value that indicates whether an input device supports multitouch. |
| [IInkTablet3::get_MaximumCursors](..\msinkaut\nf-msinkaut-iinktablet3-get_maximumcursors.md) | Gets the maximum number of cursors that a tablet device supports. |
| [IInkTablet::GetPropertyMetrics](..\msinkaut\nf-msinkaut-iinktablet-getpropertymetrics.md) | Retrieves the metrics data for a specified property. |
| [IInkTablet::IsPacketPropertySupported](..\msinkaut\nf-msinkaut-iinktablet-ispacketpropertysupported.md) | Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. |
| [IInkTablet::get_HardwareCapabilities](..\msinkaut\nf-msinkaut-iinktablet-get_hardwarecapabilities.md) | Gets a bitmask that defines the hardware capabilities of the tablet, such as whether a cursor must be in physical contact with the tablet to report its position. |
| [IInkTablet::get_MaximumInputRectangle](..\msinkaut\nf-msinkaut-iinktablet-get_maximuminputrectangle.md) | Gets the maximum input rectangle, in tablet device coordinates that the IInkTablet object supports. |
| [IInkTablet::get_Name](..\msinkaut\nf-msinkaut-iinktablet-get_name.md) | Gets the name of the object. |
| [IInkTablet::get_PlugAndPlayId](..\msinkaut\nf-msinkaut-iinktablet-get_plugandplayid.md) | Gets a string representation of the Plug and Play identifier of the IInkTablet object. |
| [IInkTablets::IsPacketPropertySupported](..\msinkaut\nf-msinkaut-iinktablets-ispacketpropertysupported.md) | Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. |
| [IInkTablets::Item](..\msinkaut\nf-msinkaut-iinktablets-item.md) | Retrieves the IInkTablet object at the specified index within the InkTablets collection. |
| [IInkTablets::get_Count](..\msinkaut\nf-msinkaut-iinktablets-get_count.md) | Gets the number of objects or collections contained in a collection. |
| [IInkTablets::get_DefaultTablet](..\msinkaut\nf-msinkaut-iinktablets-get_defaulttablet.md) | Gets the default tablet within the set of available tablets. |
| [IInkTransform::GetTransform](..\msinkaut\nf-msinkaut-iinktransform-gettransform.md) | Gets the InkTransform member data. |
| [IInkTransform::Reflect](..\msinkaut\nf-msinkaut-iinktransform-reflect.md) | Performs reflection on a transform in either horizontal or vertical directions. |
| [IInkTransform::Reset](..\msinkaut\nf-msinkaut-iinktransform-reset.md) | Resets the transform to its default state, the identity transform. |
| [IInkTransform::Rotate](..\msinkaut\nf-msinkaut-iinktransform-rotate.md) | Changes the amount, measured in degrees, to change the rotation factor of the InkTransform object and optionally the center point of the rotation. |
| [IInkTransform::ScaleTransform](..\msinkaut\nf-msinkaut-iinktransform-scaletransform.md) | Applies the specified horizontal and vertical factors to the transform or ink. |
| [IInkTransform::SetTransform](..\msinkaut\nf-msinkaut-iinktransform-settransform.md) | Modifies the InkTransform member data. |
| [IInkTransform::Shear](..\msinkaut\nf-msinkaut-iinktransform-shear.md) | Adjusts the shear of the InkTransform by the specified horizontal and vertical factors. |
| [IInkTransform::Translate](..\msinkaut\nf-msinkaut-iinktransform-translate.md) | Applies a translation to a transform. |
| [IInkTransform::get_Data](..\msinkaut\nf-msinkaut-iinktransform-get_data.md) | Gets or sets access to the XFORM structure. |
| [IInkTransform::get_eDx](..\msinkaut\nf-msinkaut-iinktransform-get_edx.md) | Gets or sets the element in the third row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::get_eDy](..\msinkaut\nf-msinkaut-iinktransform-get_edy.md) | Gets or sets the element in the third row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::get_eM11](..\msinkaut\nf-msinkaut-iinktransform-get_em11.md) | Gets or sets the element in the first row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::get_eM12](..\msinkaut\nf-msinkaut-iinktransform-get_em12.md) | Gets or sets the element in the first row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::get_eM21](..\msinkaut\nf-msinkaut-iinktransform-get_em21.md) | Gets or sets the element in the second row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::get_eM22](..\msinkaut\nf-msinkaut-iinktransform-get_em22.md) | Gets or sets the element in the second row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_Data](..\msinkaut\nf-msinkaut-iinktransform-put_data.md) | Gets or sets access to the XFORM structure. |
| [IInkTransform::put_eDx](..\msinkaut\nf-msinkaut-iinktransform-put_edx.md) | Gets or sets the element in the third row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_eDy](..\msinkaut\nf-msinkaut-iinktransform-put_edy.md) | Gets or sets the element in the third row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_eM11](..\msinkaut\nf-msinkaut-iinktransform-put_em11.md) | Gets or sets the element in the first row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_eM12](..\msinkaut\nf-msinkaut-iinktransform-put_em12.md) | Gets or sets the element in the first row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_eM21](..\msinkaut\nf-msinkaut-iinktransform-put_em21.md) | Gets or sets the element in the second row, first column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkTransform::put_eM22](..\msinkaut\nf-msinkaut-iinktransform-put_em22.md) | Gets or sets the element in the second row, second column of the affine transform matrix that is represented by an InkTransform object. |
| [IInkWordList2::AddWords](..\msinkaut\nf-msinkaut-iinkwordlist2-addwords.md) | Adds more than one word to an InkWordList in a single operation. |
| [IMathInputControl::AddFunctionName](..\micaut\nf-micaut-imathinputcontrol-addfunctionname.md) | Adds a new function-name definition to the list of custom math functions that the recognizer accepts. |
| [IMathInputControl::Clear](..\micaut\nf-micaut-imathinputcontrol-clear.md) | Clears all ink from the control. |
| [IMathInputControl::EnableAutoGrow](..\micaut\nf-micaut-imathinputcontrol-enableautogrow.md) | Determines whether the control automatically grows when input is entered beyond the control's current range. |
| [IMathInputControl::EnableExtendedButtons](..\micaut\nf-micaut-imathinputcontrol-enableextendedbuttons.md) | Determines whether the extended set of control buttons is shown. |
| [IMathInputControl::GetHoverIcon](..\micaut\nf-micaut-imathinputcontrol-gethovericon.md) | Retrieves the icon to be used for the hover target to launch math input control. |
| [IMathInputControl::GetPosition](..\micaut\nf-micaut-imathinputcontrol-getposition.md) | Retrieves the position and size of the control. |
| [IMathInputControl::GetPreviewHeight](..\micaut\nf-micaut-imathinputcontrol-getpreviewheight.md) | Retrieves the height in pixels of the preview area. |
| [IMathInputControl::Hide](..\micaut\nf-micaut-imathinputcontrol-hide.md) | Hides the control. |
| [IMathInputControl::IsVisible](..\micaut\nf-micaut-imathinputcontrol-isvisible.md) | Determines whether the control is visible. |
| [IMathInputControl::LoadInk](..\micaut\nf-micaut-imathinputcontrol-loadink.md) | Processes ink and triggers recognition. |
| [IMathInputControl::RemoveFunctionName](..\micaut\nf-micaut-imathinputcontrol-removefunctionname.md) | Removes a function-name definition from the list of custom math functions that the recognizer accepts. |
| [IMathInputControl::SetCaptionText](..\micaut\nf-micaut-imathinputcontrol-setcaptiontext.md) | Modifies the string that will be used as the control's caption when the window is created. |
| [IMathInputControl::SetCustomPaint](..\micaut\nf-micaut-imathinputcontrol-setcustompaint.md) | Determines whether a button or background has custom painting. |
| [IMathInputControl::SetOwnerWindow](..\micaut\nf-micaut-imathinputcontrol-setownerwindow.md) | Modifies the window that owns this control. |
| [IMathInputControl::SetPosition](..\micaut\nf-micaut-imathinputcontrol-setposition.md) | Modifies the location and size of the control. |
| [IMathInputControl::SetPreviewHeight](..\micaut\nf-micaut-imathinputcontrol-setpreviewheight.md) | Modifies the preview-area height in pixels. |
| [IMathInputControl::Show](..\micaut\nf-micaut-imathinputcontrol-show.md) | Shows the control. |
| [IPenInputPanel::CommitPendingInput](..\peninputpanel\nf-peninputpanel-ipeninputpanel-commitpendinginput.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sends collected ink to the recognizer and posts the recognition result. |
| [IPenInputPanel::EnableTsf](..\peninputpanel\nf-peninputpanel-ipeninputpanel-enabletsf.md) | Deprecated. Gets or sets a Boolean value that indicates whether the PenInputPanel object attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface. |
| [IPenInputPanel::MoveTo](..\peninputpanel\nf-peninputpanel-ipeninputpanel-moveto.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sets the position of the PenInputPanel object to a static screen position. |
| [IPenInputPanel::Refresh](..\peninputpanel\nf-peninputpanel-ipeninputpanel-refresh.md) | Refresh is no longer available for use as of Windows XP Tablet PC Edition. |
| [IPenInputPanel::get_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_attachededitwindow.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sets or gets the window handle of the object that the PenInputPanel object is attached to. |
| [IPenInputPanel::get_Busy](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_busy.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets a a value that indicates whether the PenInputPanel object is currently processing ink. |
| [IPenInputPanel::get_CurrentPanel](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_currentpanel.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets which panel type is currently being used for input within the PenInputPanel object. |
| [IPenInputPanel::get_DefaultPanel](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_defaultpanel.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the default panel type used for input within the PenInputPanel object. |
| [IPenInputPanel::get_Factoid](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_factoid.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the string name of the factoid used by the PenInputPanel object. |
| [IPenInputPanel::get_Height](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_height.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the height of the pen input panel in client coordinates. |
| [IPenInputPanel::get_HorizontalOffset](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_horizontaloffset.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached. |
| [IPenInputPanel::get_Top](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_top.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the vertical, or y-axis, location of the top edge of the PenInputPanel object, in screen coordinates. |
| [IPenInputPanel::get_VerticalOffset](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_verticaloffset.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the closest horizontal edge of the pen input panel and the closest horizontal edge of the control to which it is attached. |
| [IPenInputPanel::get_Visible](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_visible.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets a value that indicates whether the PenInputPanel object is visible. |
| [IPenInputPanel::get_Width](..\peninputpanel\nf-peninputpanel-ipeninputpanel-get_width.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets the width of the pen input panel in client coordinates. |
| [IPenInputPanel::put_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_attachededitwindow.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sets or gets the window handle of the object that the PenInputPanel object is attached to. |
| [IPenInputPanel::put_CurrentPanel](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_currentpanel.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets which panel type is currently being used for input within the PenInputPanel object. |
| [IPenInputPanel::put_DefaultPanel](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_defaultpanel.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the default panel type used for input within the PenInputPanel object. |
| [IPenInputPanel::put_Factoid](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_factoid.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the string name of the factoid used by the PenInputPanel object. |
| [IPenInputPanel::put_HorizontalOffset](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_horizontaloffset.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the left edge of the pen input panel and the left edge of the control to which it is attached. |
| [IPenInputPanel::put_VerticalOffset](..\peninputpanel\nf-peninputpanel-ipeninputpanel-put_verticaloffset.md) | Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Gets or sets the offset between the closest horizontal edge of the pen input panel and the closest horizontal edge of the control to which it is attached. |
| [IRealTimeStylus2::get_FlicksEnabled](..\rtscom\nf-rtscom-irealtimestylus2-get_flicksenabled.md) | Returns a value indicating whether flick gestures are enabled for the RTS. |
| [IRealTimeStylus2::put_FlicksEnabled](..\rtscom\nf-rtscom-irealtimestylus2-put_flicksenabled.md) | Indicates if flick gesture recognition is enabled. |
| [IRealTimeStylus3::get_MultiTouchEnabled](..\rtscom\nf-rtscom-irealtimestylus3-get_multitouchenabled.md) | Indicates whether the IRealTimeStylus3 object has multitouch input enabled. |
| [IRealTimeStylus3::put_MultiTouchEnabled](..\rtscom\nf-rtscom-irealtimestylus3-put_multitouchenabled.md) | Indicates whether the IRealTimeStylus3 object has multitouch input enabled. |
| [IRealTimeStylus::AddCustomStylusDataToQueue](..\rtscom\nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue.md) | Adds custom data to the specified queue of the RealTimeStylus Class object. |
| [IRealTimeStylus::AddStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-addstylusasyncplugin.md) | Adds an IStylusAsyncPlugin to the asynchronous plug-in collection at the specified index. |
| [IRealTimeStylus::AddStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-addstylussyncplugin.md) | Adds an IStylusSyncPlugin to the synchronous plug-in collection at the specified index. |
| [IRealTimeStylus::ClearStylusQueues](..\rtscom\nf-rtscom-irealtimestylus-clearstylusqueues.md) | Clears the RealTimeStylus Class input and output queues of data. |
| [IRealTimeStylus::GetAllTabletContextIds](..\rtscom\nf-rtscom-irealtimestylus-getalltabletcontextids.md) | Retrieves an array containing all of the currently active tablet context identifiers. |
| [IRealTimeStylus::GetDesiredPacketDescription](..\rtscom\nf-rtscom-irealtimestylus-getdesiredpacketdescription.md) | Retrieves the list of properties that have been requested to be included in the packet stream. |
| [IRealTimeStylus::GetPacketDescriptionData](..\rtscom\nf-rtscom-irealtimestylus-getpacketdescriptiondata.md) | Retrieves the packet properties and scaling factors. |
| [IRealTimeStylus::GetStylusAsyncPluginCount](..\rtscom\nf-rtscom-irealtimestylus-getstylusasyncplugincount.md) | Retrieves the number of plug-ins in the asynchronous plug-in collection. |
| [IRealTimeStylus::GetStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-getstylusasyncplugin.md) | Retrieves the plug-in at the specified index in the asynchronous plug-in collection. |
| [IRealTimeStylus::GetStylusForId](..\rtscom\nf-rtscom-irealtimestylus-getstylusforid.md) | Retrieves a stylus for the specified stylus identifier. |
| [IRealTimeStylus::GetStylusSyncPluginCount](..\rtscom\nf-rtscom-irealtimestylus-getstylussyncplugincount.md) | Retrieves the number of plug-ins in the synchronous plug-in collection. |
| [IRealTimeStylus::GetStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-getstylussyncplugin.md) | Retrieves the plug-in at the specified index in the synchronous plug-in collection. |
| [IRealTimeStylus::GetStyluses](..\rtscom\nf-rtscom-irealtimestylus-getstyluses.md) | Retrieves the collection of styluses the RealTimeStylus Class object has encountered. |
| [IRealTimeStylus::GetTabletContextIdFromTablet](..\rtscom\nf-rtscom-irealtimestylus-gettabletcontextidfromtablet.md) | Retrieves the TabletContextId property that is associated with a given tablet digitizer object. |
| [IRealTimeStylus::GetTabletFromTabletContextId](..\rtscom\nf-rtscom-irealtimestylus-gettabletfromtabletcontextid.md) | Retrieves an IInkTablet Interface for a specified tablet context. |
| [IRealTimeStylus::GetTablet](..\rtscom\nf-rtscom-irealtimestylus-gettablet.md) | Retrieves an IInkTablet Interface object to the caller. |
| [IRealTimeStylus::RemoveAllStylusAsyncPlugins](..\rtscom\nf-rtscom-irealtimestylus-removeallstylusasyncplugins.md) | Removes all the plug-ins from the asynchronous plug-in collection. |
| [IRealTimeStylus::RemoveAllStylusSyncPlugins](..\rtscom\nf-rtscom-irealtimestylus-removeallstylussyncplugins.md) | Removes all of the plug-ins from the synchronous plug-in collection. |
| [IRealTimeStylus::RemoveStylusAsyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-removestylusasyncplugin.md) | Removes and optionally returns an IStylusAsyncPlugin with the specified index in the asynchronous plug-in collection. |
| [IRealTimeStylus::RemoveStylusSyncPlugin](..\rtscom\nf-rtscom-irealtimestylus-removestylussyncplugin.md) | Removes an IStylusSyncPlugin from the collection at the specified index. |
| [IRealTimeStylus::SetAllTabletsMode](..\rtscom\nf-rtscom-irealtimestylus-setalltabletsmode.md) | Sets the mode for the RealTimeStylus Class object to collect data from all digitizers. |
| [IRealTimeStylus::SetDesiredPacketDescription](..\rtscom\nf-rtscom-irealtimestylus-setdesiredpacketdescription.md) | Requests properties to be included in the packet stream. |
| [IRealTimeStylus::SetSingleTabletMode](..\rtscom\nf-rtscom-irealtimestylus-setsingletabletmode.md) | Modifies the mode for RealTimeStylus Class (RTS) object to collect input from only one tablet object representing a digitizer attached to the Tablet PC. Stylus input from other digitizers is ignored by the RealTimeStylus. |
| [IRealTimeStylus::get_ChildRealTimeStylusPlugin](..\rtscom\nf-rtscom-irealtimestylus-get_childrealtimestylusplugin.md) | Gets or sets a RealTimeStylus object as an asynchronous plug-in of the current RealTimeStylus object. |
| [IRealTimeStylus::get_Enabled](..\rtscom\nf-rtscom-irealtimestylus-get_enabled.md) | Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data. |
| [IRealTimeStylus::get_HWND](..\rtscom\nf-rtscom-irealtimestylus-get_hwnd.md) | Gets or sets the handle value associated with the window the RealTimeStylus object uses. |
| [IRealTimeStylus::get_WindowInputRectangle](..\rtscom\nf-rtscom-irealtimestylus-get_windowinputrectangle.md) | Gets or sets the window input rectangle for the RealTimeStylus Class object. |
| [IRealTimeStylus::put_Enabled](..\rtscom\nf-rtscom-irealtimestylus-put_enabled.md) | Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data. |
| [IRealTimeStylus::put_HWND](..\rtscom\nf-rtscom-irealtimestylus-put_hwnd.md) | Gets or sets the handle value associated with the window the RealTimeStylus object uses. |
| [IRealTimeStylus::put_WindowInputRectangle](..\rtscom\nf-rtscom-irealtimestylus-put_windowinputrectangle.md) | Gets or sets the window input rectangle for the RealTimeStylus Class object. |
| [IRealTimeStylusSynchronization::AcquireLock](..\rtscom\nf-rtscom-irealtimestylussynchronization-acquirelock.md) | Retrieves the specified lock. |
| [IRealTimeStylusSynchronization::ReleaseLock](..\rtscom\nf-rtscom-irealtimestylussynchronization-releaselock.md) | Releases the specified lock. |
| [IStrokeBuilder::AppendPackets](..\rtscom\nf-rtscom-istrokebuilder-appendpackets.md) | Adds a packet to the end of the digitizer input packet list. |
| [IStrokeBuilder::BeginStroke](..\rtscom\nf-rtscom-istrokebuilder-beginstroke.md) | Begins a stroke on an ink object by using packet data from a RealTimeStylus Class object. |
| [IStrokeBuilder::CreateStroke](..\rtscom\nf-rtscom-istrokebuilder-createstroke.md) | Creates strokes on an ink object by using packet data that came from a RealTimeStylus Class object. |
| [IStrokeBuilder::EndStroke](..\rtscom\nf-rtscom-istrokebuilder-endstroke.md) | Ends a stroke and returns the stroke object. |
| [IStrokeBuilder::get_Ink](..\rtscom\nf-rtscom-istrokebuilder-get_ink.md) | Gets or sets the ink object that is associated with the IStrokeBuilder object. |
| [IStylusPlugin::CustomStylusDataAdded](..\rtscom\nf-rtscom-istylusplugin-customstylusdataadded.md) | Notifies the implementing plug-in that custom stylus data is available. |
| [IStylusPlugin::DataInterest](..\rtscom\nf-rtscom-istylusplugin-datainterest.md) | Retrieves the events for which the plug-in is to receive notifications. |
| [IStylusPlugin::Error](..\rtscom\nf-rtscom-istylusplugin-error.md) | Notifies the implementing object that this plug-in or one of the previous plug-ins in either the IStylusAsyncPlugin or IStylusSyncPlugin collection threw an exception. |
| [IStylusPlugin::InAirPackets](..\rtscom\nf-rtscom-istylusplugin-inairpackets.md) | Notifies the object implementing the plug-in that the stylus is moving above the digitizer. |
| [IStylusPlugin::Packets](..\rtscom\nf-rtscom-istylusplugin-packets.md) | Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer. |
| [IStylusPlugin::RealTimeStylusDisabled](..\rtscom\nf-rtscom-istylusplugin-realtimestylusdisabled.md) | Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is disabled. |
| [IStylusPlugin::RealTimeStylusEnabled](..\rtscom\nf-rtscom-istylusplugin-realtimestylusenabled.md) | Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is enabled. |
| [IStylusPlugin::StylusButtonDown](..\rtscom\nf-rtscom-istylusplugin-stylusbuttondown.md) | Notifies the implementing plug-in that the user is pressing a stylus button. |
| [IStylusPlugin::StylusButtonUp](..\rtscom\nf-rtscom-istylusplugin-stylusbuttonup.md) | Notifies the implementing plug-in that the user has released a stylus button. |
| [IStylusPlugin::StylusDown](..\rtscom\nf-rtscom-istylusplugin-stylusdown.md) | Notifies the implementing plug-in that the tablet pen has touched the digitizer surface. |
| [IStylusPlugin::StylusInRange](..\rtscom\nf-rtscom-istylusplugin-stylusinrange.md) | Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer. |
| [IStylusPlugin::StylusOutOfRange](..\rtscom\nf-rtscom-istylusplugin-stylusoutofrange.md) | Notifies the implementing plug-in that the stylus has left the detection range of the digitizer. |
| [IStylusPlugin::StylusUp](..\rtscom\nf-rtscom-istylusplugin-stylusup.md) | Notifies the implementing plug-in that the user has raised the tablet pen from the tablet digitizer surface. |
| [IStylusPlugin::SystemEvent](..\rtscom\nf-rtscom-istylusplugin-systemevent.md) | Notifies the implementing plug-in that a system event is available. |
| [IStylusPlugin::TabletAdded](..\rtscom\nf-rtscom-istylusplugin-tabletadded.md) | Notifies an implementing plug-in when an ITablet object is attached to the system. |
| [IStylusPlugin::TabletRemoved](..\rtscom\nf-rtscom-istylusplugin-tabletremoved.md) | Notifies an implementing plug-in when an ITablet object is removed from the system. |
| [IStylusPlugin::UpdateMapping](..\rtscom\nf-rtscom-istylusplugin-updatemapping.md) | Notifies the plug-in when display properties, such as dpi or orientation, change. |
| [ITextInputPanel::Advise](..\peninputpanel\nf-peninputpanel-itextinputpanel-advise.md) | Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object. |
| [ITextInputPanel::CommitPendingInput](..\peninputpanel\nf-peninputpanel-itextinputpanel-commitpendinginput.md) | Sends collected ink to the recognizer and posts the recognition result. |
| [ITextInputPanel::SetInPlaceHoverTargetPosition](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplacehovertargetposition.md) | Explicitly positions the Tablet PC Input Panel hover target in screen coordinates. |
| [ITextInputPanel::SetInPlacePosition](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplaceposition.md) | Explicitly positions the Tablet PC Input Panel in screen coordinates. |
| [ITextInputPanel::SetInPlaceVisibility](..\peninputpanel\nf-peninputpanel-itextinputpanel-setinplacevisibility.md) | Shows or hides the Tablet PC Input Panel. |
| [ITextInputPanel::Unadvise](..\peninputpanel\nf-peninputpanel-itextinputpanel-unadvise.md) | Terminates an advisory connection previously established through ITextInputPanel |
| [ITextInputPanel::get_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_attachededitwindow.md) | Gets or sets the window handle of the object to which the ITextInputPanel object is attached. |
| [ITextInputPanel::get_CurrentCorrectionMode](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentcorrectionmode.md) | Gets the current correction comb mode as specified by the CorrectionMode Enumeration. |
| [ITextInputPanel::get_CurrentInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinplacestate.md) | Gets the current in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::get_CurrentInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinputarea.md) | Gets the current input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::get_CurrentInteractionMode](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_currentinteractionmode.md) | Gets the positioning of the Tablet PC Input Panel as specified by the InteractionMode Enumeration. |
| [ITextInputPanel::get_DefaultInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_defaultinplacestate.md) | Gets or sets the default in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::get_DefaultInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_defaultinputarea.md) | Gets or sets the default input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::get_ExpandPostInsertionCorrection](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_expandpostinsertioncorrection.md) | Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded. |
| [ITextInputPanel::get_InPlaceBoundingRectangle](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_inplaceboundingrectangle.md) | Gets the bounding rectangle for Tablet PC Input Panel. |
| [ITextInputPanel::get_InPlaceVisibleOnFocus](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_inplacevisibleonfocus.md) | Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus. |
| [ITextInputPanel::get_PopDownCorrectionHeight](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_popdowncorrectionheight.md) | Gets the height of the Post-Insertion correction comb when it is positioned below Input Panel. |
| [ITextInputPanel::get_PopUpCorrectionHeight](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_popupcorrectionheight.md) | Gets the height of the Post-Insertion correction comb when it is positioned above Input Panel. |
| [ITextInputPanel::get_PreferredInPlaceDirection](..\peninputpanel\nf-peninputpanel-itextinputpanel-get_preferredinplacedirection.md) | Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field. |
| [ITextInputPanel::put_AttachedEditWindow](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_attachededitwindow.md) | Gets or sets the window handle of the object to which the ITextInputPanel object is attached. |
| [ITextInputPanel::put_DefaultInPlaceState](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_defaultinplacestate.md) | Gets or sets the default in-place state as specified by the InPlaceState Enumeration. |
| [ITextInputPanel::put_DefaultInputArea](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_defaultinputarea.md) | Gets or sets the default input area as specified by the PanelInputArea Enumeration. |
| [ITextInputPanel::put_ExpandPostInsertionCorrection](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_expandpostinsertioncorrection.md) | Gets or sets a value that indicates whether the correction comb on the Tablet PC Input Panel is automatically expanded. |
| [ITextInputPanel::put_InPlaceVisibleOnFocus](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_inplacevisibleonfocus.md) | Gets or sets a value that indicates whether the Tablet PC Input Panel is displayed automatically when the window to which it is attached gets focus. |
| [ITextInputPanel::put_PreferredInPlaceDirection](..\peninputpanel\nf-peninputpanel-itextinputpanel-put_preferredinplacedirection.md) | Gets or sets the preferred direction of the in-place Input Panel relative to the text entry field. |
| [ITextInputPanelEventSink::CorrectionModeChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-correctionmodechanged.md) | Occurs when the correction comb on the Tablet PC Input Panel has changed modes. |
| [ITextInputPanelEventSink::CorrectionModeChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-correctionmodechanging.md) | Occurs when the correction comb on the Tablet PC Input Panel is about to change modes. |
| [ITextInputPanelEventSink::InPlaceSizeChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged.md) | Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change. |
| [ITextInputPanelEventSink::InPlaceSizeChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging.md) | Occurs when the in-place Input Panel size is about to change due to a user resize, auto growth, or an input area change. |
| [ITextInputPanelEventSink::InPlaceStateChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacestatechanged.md) | Occurs when the In-Place state has changed. |
| [ITextInputPanelEventSink::InPlaceStateChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacestatechanging.md) | Occurs when the In-Place state is about to change. |
| [ITextInputPanelEventSink::InPlaceVisibilityChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged.md) | Occurs when the Tablet PC Input Panel has switched between visible and invisible. |
| [ITextInputPanelEventSink::InPlaceVisibilityChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanging.md) | Occurs when the Tablet PC Input Panel is about to switch between visible and invisible. |
| [ITextInputPanelEventSink::InputAreaChanged](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inputareachanged.md) | Occurs when the input area has changed on the Tablet PC Input Panel. |
| [ITextInputPanelEventSink::InputAreaChanging](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-inputareachanging.md) | Occurs when the input area is about to change on the Tablet PC Input Panel. |
| [ITextInputPanelEventSink::TextInserted](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-textinserted.md) | Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel. |
| [ITextInputPanelEventSink::TextInserting](..\peninputpanel\nf-peninputpanel-itextinputpaneleventsink-textinserting.md) | Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel. |
| [ITextInputPanelRunInfo::IsTipRunning](..\peninputpanel\nf-peninputpanel-itextinputpanelruninfo-istiprunning.md) | Indicates if the Tablet PC Input Panel is running at the time the method is called. |
